# No Mouse, Just Keyboard

## Blind screen reader users use the keyboard only

With very few exceptions, blind people use only the keyboard. Why don't blind people use a mouse? Because they can't see where the mouse pointer is. A mouse is for visual spatial navigation, and given that blind users have little or no visual capabilities, a mouse simply isn't very useful to them. They use the keyboard instead.

Admittedly, there are groups of people who may use a mouse with a screen reader, such as people with low vision, or people with reading disabilities. Still, the largest group of screen reader users—the blind users—uses only a keyboard.

## Everything must be keyboard-accessible

The implication for developers is that all features and controls must be available to the keyboard. Keyboard accessibility requires several things (other modules cover this in more detail). Here are some of the highlights:

- Users must be able to tab to all controls (links, buttons, form elements, etc.).
- Users must be able to activate all links with the enter key.
- Users must be able to activate all buttons with the enter key and the space bar.
- Mouse hover features must have equivalent keyboard event handlers.
- When items are hidden from sighted users (such as drop-down menus), users must not be able to tab to the hidden items (they must be unavailable to the keyboard until activated by the user or by the script).
- When a popup dialog appears, the keyboard focus must go to the dialog. When the dialog closes, the focus must go back to the original control that activated it (or to another logical location if that control is no longer available or is not the best location).
- Custom JavaScript widgets should adhere to the ARIA Authoring Practices opens in a new window for keyboard behaviors.
- Pages must not have any keyboard traps (users must be able to get into and out of all JavaScript widgets).
- The tab order through controls must be logical.
