# Live Regions

Overview
The `aria-live` attribute allows you to make announcements to screen reader users, independent of what the user does. In other words, you don't have to wait for the user to activate a feature on the web page (e.g. click a button or move focus to or away from a particular element). You can push an `aria-live` announcement to the user at any time, based on a timer, a user action, the result of a server process, or based on pretty much any other event trigger that you like. These announcements may be visible on the screen, but they do not need to be. Usually these announcements are not accompanied by a change in the focus, but in somewhat rare circumstances, the focus may change also.

The basic idea behind an ARIA live announcement is to create an empty container, which sits and waits for text to be injected into it via JavaScript. The browser and the accessibility API are aware that the container is there, and that it is designated as a live region. As soon as text is injected into the live region, the accessibility API pushes this information to the screen reader, and the screen reader makes the announcement.

## Good example: ARIA live announcement

```html
<div aria-live="polite"></div>

<!-- event occurs, filling that container -->
<div aria-live="polite">Hello, screen reader user!</div>
```

After the proper event trigger (which varies depending on what's happening on the page), text will be injected into the container. In the example below, the screen reader will say "Hello, screen reader user!"

## Assertive vs polite

There are two ways in which an aria-live announcement can be made: assertive or polite.

### Assertive

An assertive announcement — designated by aria-live="assertive" — will interrupt a screen reader if it is in the middle of reading text, and read the aria-live announcement.

Whatever the screen reader had been reading will be truncated and will not automatically continue after the aria-live announcement. The user can choose to re-read the same content that was being read previously or choose to move on to other things. 

Screen readers may not put an assertive announcement in a queue, so if multiple assertive announcements occur simultaneously or in rapid succession, the announcements may interrupt each other, and the user may not hear the full text of the interrupted announcement(s).

### Polite

A polite announcement, designated by aria-live="polite" — will put the announcement in a queue, and then read the announcement after the screen reader is done reading the text currently in the queue.

In principle, this means that if multiple polite announcements occur simultaneously or in rapid succession, the user should eventually hear all of them, as long as the user does not interrupt the live announcements by activating other screen reader features.

## ARIA live announcements SHOULD be brief.

If a user interrupts an ARIA live announcement — for example, by pressing on the Control key (to make it stop talking), or pressing the tab key to go to the next focusable item, etc. — the announcement cannot be recovered. Screen readers (at this time) do not have an option to re-read live announcements.

If anything interrupts the live announcement, or if the user is not paying attention well enough, the announcement doesn't serve its purpose. That's just the way ARIA live announcements work.

Given this inherent limitation in live announcements, it's best to keep the announcement brief. Otherwise, the user and/or the web page or screen reader is likely to interrupt the announcement before it is over, which makes the announcement useless.

## The ARIA live region MUST be empty to begin with.

If the ARIA live region container is filled with text (inner text between the opening and closing tags) on page load or when the live region is added to the DOM, the accessibility API will not announce the inner text.

Live announcements only work properly when the accessibility API recognizes a change to the live region. Pre-existing text will not register as a change, so screen readers will not announce anything.

## The ARIA live region MUST be recognized by the accessibility API before text can be injected into it.

The best practice is to include an empty live region container in the document on page load. That is the safest way to ensure that the accessibility API registers the container as a live region. It is possible to add a live region to the DOM later, as long as the region is empty when it is added.

If the region is added to the DOM without a page refresh event, insert a delay with JavaScript before attempting to inject any announcement into it.

You'll need to experiment with the duration of the pause. Test on a variety of screen readers and browsers, including mobile devices, before deciding on a minimum delay duration. Chances are that at least 2 seconds will be required across all combinations, but other factors may come into play.

## Modifier attributes for `aria-live` regions

### `aria-atomic`

The `aria-atomic` attribute lets the assistive technology know if a whole region needs to be reread to a user, or just the change.

#### `aria-atomic="false"`

This is the default. It means that when there is a change in the region, that change can be presented on its own. When a live region is updated, the update can be announced on its own and still make sense. For example, a news headline is added to a news feed.

#### `aria-atomic="true"`

Sometimes the entire live region must be read in order to give the user enough context to make sense of the update. If atomic is set to "true", it means that the whole region must be reread for each change.

### `aria-relevant`

#### `aria-relevant="all"`

All changes are relevant. Use sparingly - when overused it can be very detrimental to the usability.

#### `aria-relevant="additions"`

Insertion of nodes to the live region are relevant. For example, nodes that are removed from the top of a log are merely removed for purposes of creating room for other entries, and the removal of them does not have meaning.

#### `aria-relevant="removals"`:

Removal of nodes to the live region are relevant (i.e., a screen reader will speak the removal).
`aria-relevant="text"`

Changes to the textual content (including text equivalents, such as alt text) in the live region are relevant.


#### Note

`aria-relevant` values of removals or all are to be used sparingly. Assistive technologies only need to be informed of content removal when its removal represents an important change, such as a buddy leaving a chat room.

### `aria-busy`

There are times you may want to suppress assistive technology's announcement of presentation changes while a region is updating. To suppress announcements while the region is updating, you can use the aria-busy (state) property. Set aria-busy="true" and then clear the attribute when the region is finished.

## Different types of aria-live regions

### role="alert"

An ARIA alert (role="alert") is a special kind of assertive live region that can be used to announce important information to screen reader users. An alert is the equivalent to `aria-live="assertive"` except that some screen readers say "alert," to let users know that it is an alert message.

#### Example

```html
<form id="successForm" method="post" action="javascript:void(0)">
  <p><button>Save my preferences</button></p>
  <div class="msg" role="alert">
      <span class="msgTxt"></span>
      <!-- after using JavaScript to inject text into the alert -->
      <span class="msgTxt">Your preferences have been saved.</span>
  </div>
</form>
```

### role="status"

An element with `role="status"` will announce status updates to screen reader users. 

The status role is a special kind of live region for status updates, which are announcements that are less urgent than alerts.

Status updates have an implied `aria-live` type of polite (meaning that screen readers will wait to read the announcement until after finishing with what they are currently reading), and an implied `aria-atomic` of true (meaning that everything in the region will be announced; not just additions or subtractions).

Sometimes it can be a bit of a judgment call as to whether an announcement should be an alert, a status update, or a more generic `aria-live` announcement.

Any of these can work, but they may give users a slightly different sense of the level of urgency in the announcement, especially in screen readers that say "alert" or "status" before announcing alerts or status updates, respectively.

#### Note:

Screen readers may not distinguish between `role="status"` and `aria-live="polite"`, so the end result may sound the same to users.

### role="timer"

Setting an element to `role="timer"` designates it as time counter, either counting up or down.

This role isn't as useful as other types of live regions, because the implied value is `aria-live="off"`, meaning that screen readers are not supposed to announce changes to timers at all, though screen reader users will be able to read the content of the timer if they navigate to the timer and listen to the text.

The reason that screen readers are not supposed to announce timers is because it would be far too annoying to hear the time read out every second (or whatever the interval may be), and the announcements would interfere with the user's ability to read the rest of the web page.

Semantically-speaking, setting role="timer" on timers is the right thing to do, but it doesn't really affect accessibility either way.

### role="marquee"

Setting an element to `role="marquee"` designates it as a scrolling area (such as a news ticker) with non-essential announcements.

The implied value is `aria-live="off"`, meaning that screen readers are not supposed to announce changes in marquees at all, though screen reader users will be able to read the content of the marquee if they navigate to the marquee and listen to the text.

As with timers, marquees would be too annoying to listen to updates if they occur frequently, and the announcements would interfere with the user's ability to read the rest of the web page. Semantically-speaking, setting role="marquee" on scrolling marquees is the right thing to do, but it doesn't really affect accessibility either way.

### role="log"

Logs keep a record of sequential events, such as a chat conversation, steps in a software installation process, or other similar sequential actions.