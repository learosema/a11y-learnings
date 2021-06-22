# Value

## Overview
Properties and states need to be communicated to screen readers, and any changes need to be communicated as well. In some cases, these attributes refer to the IDs of other elements (e.g. `aria-labelledby="someID"`). In other cases the options are true or false (e.g. `aria-hidden="true"`). Some ARIA attributes are limited to predefined options (e.g. `aria-orientation="vertical"` versus `aria-orientation="horizontal"`).

In the case of dynamic widgets, the value would need to be toggled based on circumstances (e.g. `aria-expanded="true"` versus `aria-expanded="false"`). The toggling of the value does not happen automatically just by virtue of putting in the initial state or by using ARIA. You have to use JavaScript to toggle the value.

### Global

These properties and states can apply to any element on the web page, even if you don't assign an ARIA role to it.

### Properties

- `aria-atomic`
- `aria-controls`
- `aria-describedby`
- `aria-dropeffect`
- `aria-flowto`
- `aria-haspopup`
- `aria-label`
- `aria-labelledby`
- `aria-live`
- `aria-owns`
- `aria-relevant`

### States

- `aria-busy`
- `aria-disabled`
- `aria-grabbed`
- `aria-hidden`
- `aria-invalid`

## Widgets

These properties and states apply to user interface objects like alert, alertdialog, menu, progressbar, tooltip, and other widgets.

### Properties

- `aria-autocomplete`
- `aria-haspopup`
- `aria-label`
- `aria-level`
- `aria-multiline`
- `aria-multiselectable`
- `aria-orientation`
- `aria-readonly`
- `aria-required`
- `aria-sort`
- `aria-valuemax`
- `aria-valuemin`
- `aria-valuenow`
- `aria-valuetext`

### States

- `aria-checked`
- `aria-disabled`
- `aria-expanded`
- `aria-hidden`
- `aria-invalid`
- `aria-pressed`
- `aria-selected`

## Drag and Drop

These properties and states apply to elements on the page that a user can interactively move and re-order with the mouse or other input devices.

### Properties

- `aria-dropeffect`

### States

- `aria-grabbed`

## Live Regions

These properties and states apply to elements that are set to convey real-time announcements to screen reader users.

### Properties

- `aria-atomic`
- `aria-live`
- `aria-relevant`

### States

- `aria-busy`

## Related Links

See [W3C explanation of ARIA states and properties](https://www.w3.org/WAI/PF/aria-1.1/states_and_properties)