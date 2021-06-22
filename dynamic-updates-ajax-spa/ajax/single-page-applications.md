# Single Page Applications

## Overview

Single page applications were invented to speed up web sites. Rather than force a complete page refresh every time a person clicks on a link, single page applications typically load just the main content, plus a few variables, such as the page title, page-specific styles (if any), and page-specific JavaScript (if any). The two main accessibility problems that need to be solved are:

### Notifying users when new content is loaded (silence is bad).

Whenever screen reader users activate links, buttons, or controls, they need to hear some feedback. The design ought to have a standard method for handling AJAX-driven links and form submissions.

### Managing keyboard focus.

Oftentimes users click on links in DOM nodes that will be gone after the new content loads (e.g. when they click on a link in a paragraph in the main content area; that paragraph will be completely gone after the main content is overwritten with the new content).

Almost always this causes the focus to be lost completely, going back up to the top of the page. That may be partially OK in some circumstances (when going to the top of the page is desirable), but it's best to always plan for the focus to go to a specific location whenever there is a risk that the focus will be lost.

## Screen reader users SHOULD be made aware when new "pages" are loaded in single-page applications.

There are two main ways to notify the user when new AJAX content has loaded:

1. Move the focus to the new content
2. Announce the new content via aria-live

Either of these can be appropriate, depending on the circumstances, but in most simple single-page applications, it usually makes the most sense to move the focus to the new content.

### Moving the focus to the new content

Keep the following in mind when sending the focus:

#### The container MUST be set to `tabindex="-1"`. 

In order to receive the focus successfully, the container where the focus is being sent must be set to `tabindex="-1"`.

#### The focus MUST be temporarily moved, then sent to the correct destination.

If the focus is already on the element where the focus will be sent, some screen readers (VoiceOver on macOS in particular) will not read the text in the element, even if the text in the element has changed. One of the easiest ways to fix this is to temporarily send the focus to an empty container, then send it to the desired destination. Not all screen readers require the temporary focus trick, but it is a requirement (at least for now) if you plan to support VoiceOver and Safari.

#### There MUST be a delay before sending the focus to the final destination.

VoiceOver on iOS is particularly prone to losing the focus on AJAX content if the focus is sent too soon. A good delay duration is typically about 1 second, but you should test your script to ensure the delay you have chosen is sufficient. Most screen readers can tolerate much shorter delays, but iOS cannot (unless/until they fix it).

#### The focus SHOULD be sent to a heading at the beginning of the AJAX content.

If at all possible, send the focus to a heading at the beginning of the AJAX content. The heading will act essentially like the title of the new page. With single-page applications, the `<title>` won't be read by most screen readers, so having a heading that acts as a sort of substitute for the `<title>` is a good approach. 

The first `<h1>` heading in the AJAX content can be selected in JavaScript: `$("#container h1:first")`. It may also be acceptable to send the focus to the container of the new AJAX content — such as `$("#content")` — if a heading is not available.

### Announcing the new content via aria-live

In less common cases, it may be appropriate to keep the focus on the button (or control or link), rather than send the focus to the new content. If that's the case, the user still needs to hear confirmation that something happened.

#### Optional: Confirm that the action is in progress.

If there is a risk that there may be a delay in receiving the AJAX response, you could announce something like "page loading," or "searching," or "in progress," or something along those lines. This could apply to AJAX responses that retrieve content from third-party servers or database queries that might take a few seconds.

#### Confirm the result of the action (success or failure message).

Let users know that the event has finished, and that it was either successful or a failure. You could say things like "Message sent," or "Error: message could not be sent," or "Additional results loaded," etc.

#### Keep the message brief.

ARIA live messages can't be replayed, and there is a risk that the user may interrupt them, so if the message needs to be heard in its entirety, the user is more likely to listen to a short message than a long one.

#### Choose either assertive or polite.

An assertive message (aria-live="assertive") is usually appropriate when the ARIA live message is the result of the user activating a button or link, but aria-live="polite" is also an option.

#### Optional: provide (brief) instructions related to the new content.

An example would be a custom auto-complete form field that loads options as soon as the user starts typing. The announcement could say something like, "Four options available. Use down arrow to select."

### Example: link click event with single-page application accessibility techniques

```js
$(document).on('click', 'a', function (e) {  
  /* Don't let links act like regular links */
  e.preventDefault();

  /* Run functions that do the following:
    - empty the containers that the AJAX content will fill
    - load the AJAX content
    - update the document with the AJAX content
    - update the browser history
    - send the focus temporarily to an empty container
    - send the focus to the desired destination after a delay
  */
});
```

## The browser history MUST be updated when an AJAX event is the result of clicking on a link OR if the event is such that a user would expect to be able to use the "back" button after the event.

Users expect to be able to use the back button after clicking on a link or after activating a feature that seems to load a new page. On single-page applications, the browser history will not be updated unless the page includes JavaScript code to cause the browser history to change. It's something that has to be planned and implemented in a systematic way.

### Example

```js
var newUrl = 'https://dequeuniversity.com';
var newTitle = 'Deque University';
history.pushState({
  url: newUrl,
  title: newTitle
}, newTitle, newUrl);
```

## The page MUST respond appropriately when the user activates back or forward functionality in the browser.

The browser sends a `popstate` event when the "Back" or "Forward" buttons (or keyboard commands) are activated in the browser. You can intercept that event and apply the appropriate accessibility techniques.

### Example

```js
$(window).on('popstate', function (e) {
  var state = e.originalEvent.state;
  if (state !== null) {
    /* 
    Run functions that do the following:
    - empty the containers that the AJAX content will fill
    - load the AJAX content
    - update the document with the AJAX content
    - send the focus temporarily to an empty container
    - send the focus to the desired destination after a delay
    */
  } 
  else {
    /* 
    (optional conditions when a popstate
    is not activated)
    */
   } 
 });
```

## Putting it all together

[Single-page application example](https://dequeuniversity.com/assets/html/module-dynamic/singlepage/good/index.html)

```js
$(function () {

  var currentContent = $('#innerContent');
  var currentHeading = $('#contentHeading');
  var newTitle;
  var newHeading;
  var newContent;

  var load = function (newUrl) {
    /* get AJAX content */
    $.get(newUrl).done(function (data) {
	
    /* Parse the page into variables to insert separately */
    newTitle = $(data).filter('title').html();
    var newMain = $(data).filter('main').html();
    newHeading = $(newMain).filter('h1').html();
    newContent = $(newMain).filter('#innerContent').html();
		
    /* update document with AJAX content variables */
    document.title = newTitle;
    currentContent.html(newContent);
    currentHeading.html(newHeading);	
    });
  }

  function focusH1(){
    /* Set focus temporarily on an empty div, 
	to force screen readers (especially VoiceOver)
	to read the focused item if the focus was already
	on that same item before we re-sent the focus to it */
    $('#tempFocus').focus();
	  
    /* Set focus on the h1 at the beginning of the content
    after a brief delay (the delay is mostly for iOS;
    sometimes shorter delays work, but they are risky 
    in iOS, so a minimum of 1 second is recommended) */
    setTimeout(function(){ 
      currentHeading.focus(); 
    }, 1000);
  };

  function emptyOld() {
    /* empty the original content 
    that is about to be replaced
    so that iOS doesn't read old information */
    $('#contentHeading, #innerContent').empty();
  }

  $(document).on('click', 'a', function (e) {
    /* activate the functions when a link is clicked */
	  
    /* don't let links act like regular links */
    e.preventDefault();

    emptyOld();

    newUrl = $(this).attr("href");
    load(newUrl);
		
    /* update the browser history */
    history.pushState({
      url: newUrl,
      title: newTitle
    }, newTitle, newUrl);

    focusH1();
  });

  $(window).on('popstate', function (e) {
    var state = e.originalEvent.state;

    if (state !== null) {
      /* activate the functions if a popstate is detected,
      e.g. if "back" or "forward" are used in the browser */

      emptyOld();

      document.title = state.title;

      load(state.url);
			
      focusH1();
    } 
		
    else {
      /* if the page loads normally 
      (not by clicking on a link or by 
      using the back/forward buttons) */
    }		
  });
});
```