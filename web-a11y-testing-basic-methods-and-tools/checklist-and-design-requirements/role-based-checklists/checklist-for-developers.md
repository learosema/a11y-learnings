# Checklist for Developers

## Semantics and Structure

- When possible, are HTML tags used and applied for their native semantics?
- Can structure, information, and relationships conveyed through visual presentation (in headings, lists, menus, forms, etc.) be programmatically determined?

## Readability

- Has the reading order been tested to confirm that all content on the page is available in a logical order for assistive technologies?

## Images

- Do all linked, informative, and decorative `<img>` elements have appropriate alternative text (e.g., alt attributes)?
- Do all informative background images have alternative text that can be read by assistive technologies?

## Keyboard and Touchscreen Navigation

- When interacting with a page with the keyboard, is focus always visible, is it managed when necessary, and does it follow a logical order?
- Can all functionality be accomplished using only the keyboard?
- Do all keyboard-only (and touchscreen) interactions follow expected patterns so users know how to interact with all widgets on the page?
- Can keyboard-only users always move focus without ever getting trapped?

## Tables

- Are data tables marked up to convey the correct relationships between data cells and their associated column or row header cells?
- Do layout tables contain only `<td>` cells and no other structural markup such as a `<th>` or `<caption>` tag?

## Form Labels

- Do form controls have visible labels? Are the label and control programmatically associated?
- Are related fields grouped and associated with a common label (if present)?

## Form Errors

- Are error descriptions programmatically associated with their form element?
- If an error is detected on form submission, are screen reader users made aware of it?
- If a validation error occurs during user input or when a user moves focus, is the error message spoken by a screen reader?

## Custom Controls

- Do all custom controls, scripted components and widgets provide names and roles to mimic native HTML controls and are they programmatically determinable?

## Context Changes

- Has it been verified that when an element receives focus, for example by tabbing to it, no major change of context is automatically triggered?
- Has it been verified that when a person changes the setting of a user interface component, no major change of context is automatically triggered unless they have been notified beforehand?

## Timing

- For scrolling, moving, blinking, dynamic or auto-updating content, are mechanisms provided to stop, pause, hide, and control it?
- Can the time limit for completing a task be turned off, adjusted, or extended by the user — unless an exception applies?
