# Visual Focus Indicator

## All focusable elements MUST have a visual focus indicator when in focus.

Browsers typically indicate which element is in focus by outlining it with either a dotted line (as in Edge, Internet Explorer, and Firefox) or a solid colored line (as in Chrome and Safari). 

The dotted line is somewhat difficult to see, especially for users with low vision, but as long as the default browser focus indicator is left intact, the visual styling is generally considered sufficient to meet the guidelines, at least in terms of minimal compliance.

### Bad example

```css 
a:focus {
  outline: none;
}
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

### Good example

```css 
a:focus {
  outline: 2px solid #8cc63f;
  background-color: #fdf6e7;
}
```

## The contrast of all visual focus indicators against the background MUST be at least 3 to 1.

In some browsers, the default styling for the visual focus indicator (the thin dotted outline around focused elements) may be difficult to see, especially for users who have low vision.

Enhancing the visual focus indicator will make it easier for users to see what element on a web page has keyboard focus among all the other elements on the web page.

Being able to detect the visual focus right away will increase the efficiency of using and interacting with the page.

## Visual Focus Indicator and High Contrast Mode

In Windows, when high contrast mode is turned on, high contrast settings may affect the look of the visual focus indicator.

### Edge and Internet Explorer

In Edge and Internet Explorer, if the visual focus indicator's outline width is enhanced and is set to display a solid line, a solid line with the outline's width will be displayed in high contrast mode.

However, if the high contrast theme has a black background, the visual focus indicator will become a white solid line. If the background is white, the visual focus indicator becomes a black solid line.

#### Note: Background colors will be suppressed

It's best practice to include a border or an outline as a part of the enhanced focus indicator, because Windows High Contrast Mode retains borders and outlines, but suppresses background colors.

If the visual focus indicator isn't enhanced and the default settings are used for the focus indicator in Edge and IE, the visual focus indicator will be displayed as a dashed line around focusable elements. Again, if the background is black, the visual focus indicator will appear as a white dashed outline; and if the background is white, the visual focus indicator will become a black dashed outline.

### Firefox

In Firefox, the colors for links can be customized even when Windows High Contrast Mode is on. So, when high contrast settings are enabled, the visual focus indicator becomes the same color as the link color chosen in Firefox's color options.

If the visual focus indicator is enhanced to display as a solid line, it will display as a solid line in the same color as the link in Firefox. If it is not enhanced and the default settings are used, the visual focus indicator will display as a dashed line in the same color as the link.

Other focusable elements that are not links will either have a black or white solid or dashed line around them, depending on whether the background is black or white or focus has been enhanced like in Edge and Internet Explorer.

In all three browsers, if the visual focus is disabled (:focus {outline: none;}), the visual focus indicator is also disabled when high contrast settings are turned on.
