# Option 3: ARIA Live

## Overview
ARIA live announcements allow the web page to make announcements without loading or reloading a page or moving the focus. For custom widgets and custom events, ARIA live announcements may be the only way to communicate certain kinds of state changes or other similar events.

ARIA live regions are containers (like `<div>` or `<span>`) marked as live regions. They start out empty. When an announcement needs to be made, a JavaScript event inserts text into the ARIA live container. Screen readers speak the text.

There are two main kinds of ARIA live announcements: aria-live="assertive" and aria-live="polite". Assertive announcements are supposed to interrupt the screen reader immediately and make the announcement. 

Polite announcements are supposed to wait until the screen reader finishes reading the current sentence or item before making the announcement. The announcement gets put into a queue until the screen reader is ready.

There are also special kinds of ARIA live regions. Setting an element to role="alert" turns it into an assertive ARIA live region (the difference is that screen readers also say "alert" when reading ARIA alert messages). Refer to the [official documentation about aria-live regions](https://www.w3.org/TR/wai-aria-1.1/#aria-live) for more details.

### Example

```html
<p><button id="liveButton">Create announcement</button>
<span id="liveRegion" aria-live="assertive"></span></p>
<p><button id="liveButton">Create announcement</button></p>
<script>
$('#liveButton').click(function(){
  var live = $('#liveRegion');
  live.css({
    'display':'inline-block',
    'background-color':'#fff5bc',
    'padding':'0px 4px'
  }).text('Hooray for accessibility!');
  setTimeout(function(){ 
    live.text('');
    live.removeAttr('style');
  }, 3000);
});
</script>
```

## Accessibility Considerations

### The ARIA live region must be present and must be empty before making an announcement. 

The best approach is to ensure the ARIA live region is already on the page when the page loads. You cannot insert an ARIA live region and make an announcement at the same time. The region needs to be on the page, and the accessibility API needs to be aware that it is there and that it is empty before any announcements will be sent to the screen reader. If you insert the ARIA live region after page load, you must use JavaScript to delay (typically for at least one second) before sending any text into it to make an announcement.

### ARIA live announcements should be brief.

Screen readers allow users to interrupt ARIA live announcements. If an ARIA live announcement is interrupted, it cannot be retrieved. The announcement is lost. Short announcements are less likely to be interrupted.

### Remove the announcement soon after it is inserted (in most cases).

ARIA live announcements are frequently used to announce things that are temporary, so it makes sense for the announcement itself to be temporary. You don't want to run the risk of having a screen reader user come across the leftover stale text of an ARIA live announcement that is no longer relevant. 

The user may think that the web page is making the announcement again, when in reality they just happened to find the original announcement.

### If the announcement is not meant to be seen, hide with CSS clip.

Sometimes ARIA live announcements are intended only for screen reader users. If that's the case, use the CSS clip method to hide it only from sighted users. The CSS would look something like this:
