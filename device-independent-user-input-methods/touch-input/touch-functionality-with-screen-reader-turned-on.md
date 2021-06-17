# Touch Functionality with Screen Reader Turned On

## Functionality MUST be available using screen reader touch methods (e.g. click actions), unless the functionality cannot be accomplished in any known way using a touch device.

When you turn on a screen reader on a touch device, the screen reader disables any scripted gestures on a web page because the screen reader itself relies on gestures to function.

On iOS devices, for example, swiping to the right moves the screen reader focus to the next element, and swiping to the left moves the screen reader focus to the previous element.

Swiping up and down on iOS devices invokes other screen reader behaviors. If a web page relies on swiping actions, those actions will not work when the screen reader is turned on.

## Good example

In this example, users can swipe to the left or right to change the image, but the swipe action is not required. Click-activated buttons to the left and right of the image allow screen reader users on touch devices to access the full functionality of the script.

The buttons are also available to non-screen reader users and will work on mobile devices that don't support scripted gestures.

[Good Example: Gesture Script with Click-Activated Buttons](https://dequeuniversity.com/assets/html/module-input-methods/gestures/good.html)