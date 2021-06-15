# Keyboard accessibility

## All functionality of a media player MUST be available to keyboard users

Other modules in this series have discussed keyboard accessibility in detail, so we will just review the basic concepts here.

## All controls MUST be tab-focusable.

If the control is a native button (`<button>` or `<input type="submit">`), it will already be tab focusable. If it is a custom control, using a `<div>`, `<span>` or other non-focusable element, you will need to add tabindex="0" to make it tab focusable.

## The tab order MUST be logical

As users tab through the controls, the tab order should coincide with the visual order of the controls as much as possible.

## All controls MUST have visual focus indicators

Sighted users need to know where the keyboard focus is at all times. When they tab to a control in the media player, it should be highlighted in some way, with a border, outline, background color, or some other similar style effect.

## The functionality MUST work with the keyboard

You have to assume that a keyboard user will not use the mouse at all (whether that it is true for a given user or not). You cannot create controls that are only mouse-activated.

## The focus MUST be managed logically during interactions

When a user activates a feature, the focus must go to the most logical place. In the case of activating a dialog, for example, the focus must go to the dialog. When the user closes the dialog, the focus must go back to the button that originally activated the dialog (or, in rare cases, to a different logical location).

## Provide keyboard instructions for any unusual controls

It's best to use standard controls and methods, but if you have any custom controls that users won't be expected to know how to use, provide instructions.