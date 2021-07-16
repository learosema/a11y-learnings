# Touch Functionality with Screen Reader On

## Overview

When a screen reader is used on a touchscreen or mobile device, it overrides the standard gestures on the device and replaces them with gestures that enhance browsing and interaction for those who rely on a screen reader.

Knowing that standard gestures are replaced with those new gestures, it is critical that touch functionality on a web page does not interfere with the gestures used with the screen reader. Touch functionality must remain intact when a screen reader is used to browse and interact with a web page.

## Testing Methodology for Touch Functionality with Screen Readers

Using a screen reader on a mobile device can be a bit of a learning curve, but a screen reader must be used to effectively test for touch functionality. In the course, Accessibility Testing: Screen Readers, there is detailed information for using Talkback on Android and VoiceOver on iOS, including gestures and configuration options.

When using a screen reader on a mobile device, check that:

- Touch functionality is available when the screen reader is on, including activating links, buttons, and interacting with custom widgets.
- Custom gestures aren't the only means to interact with content on a web page. If a gesture can be used to interact with content, a touch-based alternative is provided (e.g., being able to select/click on left and right arrows as opposed to swiping left or right to view content).

## Examples

- [Bad example of gesture-only functionality](https://dequeuniversity.com/assets/html/module-input-methods/gestures/bad.html)
- [Good example of gesture plus buttons](https://dequeuniversity.com/assets/html/module-input-methods/gestures/good.html)
