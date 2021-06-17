# Touch functionality

## Functionality MUST be available using standard touch methods, unless the functionality cannot be accomplished in any known way using a touch device.

Keyboard versus click events: If you write JavaScript with event handlers that only use keystrokes (such as the left and right arrow keys, or the "C" key, or the tab key, or the enter/return key), chances are that users on touch devices will not be able to interact with your scripted content.

Touch devices rely on click events — essentially equivalent to mouse clicks — to function properly. In general, if your content is mouse-accessible with click events, it will be touch-accessible also.

Drag and drop events: You cannot rely on drag and drop features for critical operations on touch devices, because while some touch devices allow drag and drop operations, not all do.

Even on those that do support drag and drop operations, there are differences in how that kind of functionality would need to be implemented across different operating systems and versions of operating systems, making the script somewhat fragile and unreliable.

If you create drag and drop functionality, think of it as an optional enhancement to supplement the main fully-featured click functionality.

Scripted gestures: You also cannot rely on gesture actions on web pages because of the differences between operating systems and versions. Some mobile devices do not support gestures at all. Gesture functionality should be considered an optional enhancement to supplement click functionality.


### Good example

If you use native button elements, you get keyboard/mouse/touch interaction for free. The click event can be triggered by mouse click, by tap and via keyboard by hitting space or enter.

When using aria controls, you will have to implement that yourself.

```html
<button onclick="alert(1)"> Native button with click action </button>
```
