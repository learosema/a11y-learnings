# Touch Target Size

## The click/touch target size SHOULD be large enough to facilitate easy use with a finger, without risking activating an adjacent link or button.

Users with dexterity/motor disabilities will especially appreciate large touch targets. Some people experience hand tremors or imprecise hand movements. Other people cannot use their fingers at all, and must instead use other body parts, such as their knuckles, elbow, or toes.

Some of the kinds of touch targets we need to consider are:

- Links
- Menus
- Submit Buttons
- Checkboxes
- Radio buttons
- Text input fields
- Select fields (comboboxes)
- Custom widget controls (media player buttons, for example)

Touch targets should be a minimum of 9.6mm (0.38 inches) wide on the device. Ideally, they would also be at least 9.6mm tall too, but that may be harder to achieve in some cases, especially with inline links.

Given the wide variety of sizes, resolutions, and pixel densities of mobile devices, measuring 9.6mm can be a bit of a challenge. It helps to have the actual physical device, for accurate measurements, but here are some basic guidelines:

- For native apps:
  - On standard resolution devices, set the width to at least 44px (according to Apple's recommendations) or 48px (according to Google's recommendations). On Android, it's best to use the 48px size, due to Android's layout grid opens in a new window.
- On devices with double the pixel density (such as Apple Retina screens), set the width to at least 88px-96px in terms of true screen dimensions.
- On web pages:
  - Set the width to at least 44px in the CSS (Android's 48px layout grid is less relevant on the web, but it doesn't hurt to make touch targets larger). Standard resolution devices will render it at 44px and double density devices will interpolate the value and render it at the equivalent of 44px, even though the actual value will be 88px.

Refer to the How to Meet WCAG reference guide opens in a new window for more detailed info on target size.