# Touch Target Size

## Overview

Larger touch targets will greatly benefit users who experience hand tremors, imprecise hand movements, or who may need to use other parts of their bodies to trigger targets. The kinds of touch targets testers need to consider include, but aren't limited to:

- Links
- Submit Buttons
- Radio Buttons
- Menus and Menu Items
- Input Fields and Comboboxes (Select fields)
- Custom Widget Controls (media players' buttons, tabs)

## Touch Target Sizing

Ideally, touch targets should minimally be 9.6mm (0.38 inches) wide and 9.6mm tall, though the height may be more difficult to achieve when it comes to elements like inline links. Though it would help to have a mobile device to test for target size, the web page can be manipulated to check for sizing:

- Set the width to at least 44px in the CSS (Android's 48px layout grid is less relevant on the web, but it doesn't hurt to make touch targets larger). Standard resolution devices will render it at 44px and double density devices will interpolate the value and render it at the equivalent of 44px, even though the actual value will be 88px.

### Good sizings

- 44px submit button
- 48px submit button

## Testing Methodology for Touch Target Size

As mentioned before, it is best to test for touch target size on mobile devices to see if sizing meets the best practice requirements above. There are some other things that can be done to help ensure users with dexterity or motor disabilities can trigger targets.

- Responsive Design: (Desktop) If the web page is responsive, shrink the viewport of the browser down to appropriate mobile sizing (tablet and phone).
- Forms: When HTML labels are used in forms, users should be able to select the label itself to place focus on or in the form element. Test to see if the label can be selected. This is especially important for radio buttons and checkboxes as they are small in nature.
- Links (by themselves) and Buttons: Ideally, the padding around links and buttons should also be a part of the target, not just text inside. Test to see if the padding around these elements can be selected. Using only the text inside the padding makes for a smaller target.
- Links inline with text: Links that are surrounded by regular text should have enough characters to make them 9.6mm. Extra padding for height may break visual layout, so it is critical that they are wide enough to trigger.
