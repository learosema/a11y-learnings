# Device-Independent User Input Methods

## Summary

Users need to be able to interact with web content. This includes all form elements, links, JavaScript features, custom widgets, and all other types of content.

The primary methods for interacting are mouse, keyboard, touch, and voice. Other methods are available (e.g. eye tracking or single switch devices), but they all essentially make use of, or emulate, one of the other aforementioned methods.

It is important to consider all aspects of input method accessibility, including functionality, focus management in custom widgets, visual focus and hover indicators, the unavailability of JavaScript gesture actions on mobile devices when the screen reader is turned on, etc. User input method accessibility ensures that users can not only read web content, but also interact with it and submit data when necessary.

## Checklist

### Mouse Input

#### Click Target Size

- The click target size SHOULD be large enough to facilitate easy use with a mouse (including for users with tremors or limited dexterity) without risking activating an adjacent link or button.

#### Visual Hover Indicator

- An enhanced visual hover indicator SHOULD be provided.
- The mouse cursor icon on hover SHOULD correspond to the type of action allowed by the element.

#### Pointer Cancellation

- For functionality that can be operated using a single-pointer, at least one of the following MUST be true: no down-event, can abort/undo, up reversal, or essential.

### Keyboard Input

#### Tab Focusability

- Links, buttons, and interactive controls MUST be keyboard-focusable.

#### Tab Order

- The navigation order of focusable elements (links, form elements, etc.) MUST be logical and intuitive.
  tabindex of positive values SHOULD be avoided.

#### Visual Focus Indicator

- All focusable elements MUST have a visual focus indicator when in focus.
- Focusable elements SHOULD have enhanced visual focus indicator styles.
- The contrast of all small visual focus indicators (smaller than 3px by 3px) against the background SHOULD be at least 4.5 to 1.
- The contrast of all large visual focus indicators (at least 3px by 3px) against the background) SHOULD be at least 3 to 1.

#### Keyboard Functionality

- Functionality MUST be available using the keyboard, unless the functionality cannot be accomplished in any known way using a keyboard.

#### Keyboard Traps

- Keyboard focus MUST NOT be locked or trapped in a particular page element and the user MUST be able to navigate to and from all navigable page elements using only a keyboard.

#### Focus Management During Interactions

- The focus MUST be purposely moved or set (via JavaScript) onto the appropriate element when the user's action requires a change of context or location for effective keyboard or touch interaction.
- The focus MUST NOT become lost or reset to the top of the page, except when loading or re-loading a page.
- When moving or setting focus, the destination element MUST contain programmatically determinable text (either standard text or programmatically-associated text).

#### Keyboard Shortcuts

- Page-specified shortcut keys and accesskeys MUST NOT conflict with existing keyboard shortcuts in the browser, operating system, or assistive technologies.

#### Giving Users Keyboard Instructions

- When custom keyboard behavior is required to use a component, keyboard instructions MUST be provided.
- ARIA widgets that require more than just the Tab key to interact with may be confusing to users, so you MAY provide keyboard instructions.

### Touch Input

#### Touch Functionality

- Functionality MUST be available using standard touch methods, unless the functionality cannot be accomplished in any known way using a touch device.

#### Touch Functionality with Screen Reader Turned on

- Functionality MUST be available using screen reader touch methods (e.g. click actions), unless the functionality cannot be accomplished in any known way using a touch device.

#### Touch Target Size

- The click/touch target size SHOULD be large enough to facilitate easy use with a finger, without risking activating an adjacent link or button.

#### Focus Trap

Touch/gesture focus MUST NOT be locked or trapped in a particular page element and the user MUST be able to navigate to and from all navigable page elements using standard touch actions or gestures.

#### Pointer Gestures

All functionality that uses multipoint or path-based gestures for operation MUST be operable with a single pointer without a path-based gesture, unless a multipoint or path-based gesture is essential.

### Input Modalities

- Web content SHOULD NOT restrict use of input modalities available on a platform except where the restriction is essential, required to ensure the security of the content, or required to respect user settings.

### Motion, Disappearing Content, and Transitions

#### Motion Actuation

Functionality that can be operated by device or user motion MUST also be operable by user interface components and MUST allow the ability to disable motion actuation.

#### Transitions

- Transitions MUST NOT interfere with reading or interaction, unless the interference is brief.
- Transition effects SHOULD be kept to a minimum (to avoid nausea, dizziness, annoyance, etc.).
- Transitions SHOULD avoid parallax effects.

#### Moving or Disappearing Content

- Content SHOULD NOT move in a way that makes interactive elements difficult to activate.
