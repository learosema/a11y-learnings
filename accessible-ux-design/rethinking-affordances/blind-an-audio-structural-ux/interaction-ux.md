# Audio-Structural Interaction UX

## Overview

Screen reader users typically use their keyboard to interact with elements (not the mouse). Everything has to be keyboard accessible.

As users interact with elements with their keyboard, they listen to feedback from their screen reader. The main kinds of feedback they are interested in are as follows:

- Name: The name or label applied to the element. Screen readers will announce the name of most kinds of semantic elements when the user lists them, focuses on them, or reads through them.
- Description: Extra information about the element (via aria-describedby). Screen readers usually announce the description (if any) after announcing the element's name.
- Role: Identification of the kind of element they are interacting with (e.g. a text field, a tab panel widget, a tree view, a button, a link, a graphic, a dialog, etc.). Screen readers announce the role of most semantic elements.
- Value:
  - Properties: Characteristics of elements, such as aria-valuemax (on things like sliders), aria-controls, aria-owns, etc.
  - States: Changeable conditions about an element, such as aria-selected=true/false, aria-checked=true/false, aria-hidden=true/false, etc. In most cases, screen readers will read the state change automatically when the user activates a feature. For example, a screen reader will say "expanded" after the user activates a button that changes from aria-expanded="false" to aria-expanded="true". No JavaScript or live regions are required to make a screen reader announce the state change.
  - "Live" announcements: Updates


## Live events

Live events are inherently problematic for blind users. Live captions on video aren't helpful, no matter what format they're in. With professional broadcast media, the live captions are usually embedded in the video itself, as a visual element, with no actual text that a screen reader can read. Even if a text-based format is used, the same problems exist as with pre-recorded multimedia: there is no easy way to access the captions.

### Possible solution 1: 

continuous AJAX updates. One way to send useful text for live events is to post the text directly into the document in real time using AJAX. The user can then read through the text as it comes in using regular screen reader commands. The downside to this approach is that the user may reach the end of the text, then new text may be posted above the user's current location in the document. If that happens, the user would have to traverse the text backward to find the new text. That can take time, and it is confusing to try to find the starting point, especially if the text passage is long, or if multiple updates have occurred. The continuous AJAX method can work, but it isn't the most user-friendly.

### Possible solution 2: 

a "load more live text" button. It would be more user-friendly to give deafblind users the control over when to load the content with a simple button. When users activate the button, it would probably be best to send the focus to the container of the new text. The container would need to be set to tabindex="-1" in order to receive the focus successfully.