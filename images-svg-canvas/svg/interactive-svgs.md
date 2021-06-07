# Interactive SVGs

## Interactive `<svg>` objects MUST be fully keyboard-accessible.

Highlights of what it means to be fully keyboard-accessible include the following:

- All links, buttons and controls must be keyboard-focusable and usable by keyboard users.
- All focusable elements must have a visible focus indicator.
- The scripting must manage the focus when activating, deactivating, and/or dismissing features (like dialogs, menus, etc.); the focus must be sent to the proper place at the proper time.
- The `<svg>` object must not trap the keyboard focus.
- The tab order (or arrow key order, if appropriate) must be logical.
- All focusable elements must be visible on the screen (or become visible once focus lands on them).

## Interactive `<svg>` objects MUST be fully touchscreen-accessible.

Highlights of what it means to be fully touchscreen-accessible include the following:

- All mouse-only actions have a touch equivalent action.
- All keyboard-only actions have a touch equivalent action.
- All gesture-dependent actions have an equivalent non-gesture method to achieve the same result (this rule exists because screen readers override and disable page-specific gestures in most cases; a click action is best for touchscreens).


## Interactive `<svg>` objects MUST communicate the applicable name, role, and value of controls, events, and semantic elements within the `<svg>` object.

In essence, interactive `<svg>` objects must abide by the same types of accessibility principles that govern the use of custom ARIA widgets. In fact, an interactive `<svg>` object may be coded as a custom ARIA widget. Roles like button, checkbox, tablist, and others can be added to elements within ARIA widgets.

That said, support for interactive SVG, even when combined with ARIA, is sometimes spotty and must be tested thoroughly with screen readers before going live.

