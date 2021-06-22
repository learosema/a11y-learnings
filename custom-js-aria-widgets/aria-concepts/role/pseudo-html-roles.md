# Pseudo HTML roles

## Overview

Another thing that ARIA allows web developers to do is to change the role of an element completely. For example, the `<p>` element is normally interpreted as a paragraph by browsers and assistive technologies. 

If you change it to `<p role="heading" aria-level="1">` the paragraph will now be interpreted as an `<h1>` element. Screen readers will say "heading level 1" before reading the content with the element, and for all intents and purposes, the element is no longer a paragraph at all, at least to screen reader users.

It is an `<h1>`. Similarly, you could use `<span role="checkbox">` to create a custom checkbox or `<span role="link">` to create a custom link. Available pseudo-HTML roles include the following:

- `button`
- `checkbox`
- `columnheader`
- `combobox`
- `contentinfo`
- `form`
- `grid`
- `gridcell`
- `heading`
- `img`
- `link`
- `listbox`
- `listitem`
- `option`
- `radio`
- `radiogroup`
- `row`
- `rowgroup`
- `rowheader`
- `scrollbar`
- `textbox`

## Note: Don't Reassign Roles Unless You Have To

Once web developers learn they can reassign the roles of elements, they sometimes go crazy with the idea and use ARIA roles instead of the built-in semantic markup available in regular unmodified HTML. 

It's almost always best to use regular HTML whenever possible, because no functionality is associated with the role attribute other than to communicate the role itself.

If you create a custom checkbox, for example, assigning role="checkbox" is not enough to re-create the functionality of a checkbox. You need to write JavaScript that re-creates all the keyboard and mouse functionality and logic associated with checkboxes. Why not just use a real checkbox instead?