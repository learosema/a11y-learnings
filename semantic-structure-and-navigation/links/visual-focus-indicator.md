# Visual focus indicator

## All focusable elements MUST have a visual focus indicator when in focus.
Browsers typically indicate which element is in focus by outlining it with either a dotted line (as in Edge, Internet Explorer, and Firefox) or a solid colored line (as in Chrome and Safari). 

The dotted line is somewhat difficult to see, especially for users with low vision, but as long as the default browser focus indicator is left intact, the visual styling is generally considered sufficient to meet the guidelines, at least in terms of minimal compliance.

### Bad example

Don't use 

```css
a:focus { outline: none; }
```

## Focusable elements SHOULD have enhanced visual focus indicator styles.

Although not typically required for minimum compliance with guidelines, users with low vision can benefit greatly from enhanced visual focus indicators on links, buttons, form elements, and other focusable items. Enhancements can include a different background color, different font color, outline, or border.

When creating enhanced visual focus indicators, consider all of the following:

- links — a:focus {...}
- buttons — button:focus {...}
- inputs — note that a single style may be sufficient for all inputs, depending on the design (e.g. input:focus {...}, but the styles can also be specified for individual inputs:
  - text inputs — input[type=text]:focus {...}
  - image inputs — input[type=image]:focus {...}
  - submit buttons — input[type=submit]:focus {...}
  - radio buttons — input[type=radio]:focus {...}
  - All other input types
- checkboxes — input[type=checkbox]:focus {...}
- drop-down selection inputs — select:focus {...}
- textarea fields — textarea:focus {...}
- ARIA controls:
  - ARIA links — [role=link]:focus {...}
  - ARIA buttons — [role=button]:focus {...}
  - ARIA inputs — [role=radio], [role=checkbox], etc.
  - ARIA tabs — [role=tab]:focus {...}
  - All other focusable custom ARIA controls
- All other focusable items

### Good example: enhanced focus indicator

```css
a:focus {
  outline: 2px solid #8cc63f;
  background-color: #fdf6e7;
}
```
