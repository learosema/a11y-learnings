# Parent-child relationships

## Markup SHOULD adhere to required parent-child relationships of elements and attributes.

### HTML Relationships

Some elements have required children and/or parents. For example, every list item (`<li>`) must be contained within a parent list (either `<ul>` or `<ol>`).

Browsers sometimes compensate for faulty code, but the result can still be unpredictable. Screen readers expect and rely on a certain syntax to be able to communicate the semantic meaning to blind users. When the syntax is wrong, the screen readers may not be able to communicate anything meaningful.

### ARIA Relationships

The repercussions of faulty syntax with custom ARIA widgets can be especially severe because browsers do not compensate for them at all, and screen readers rely more heavily on the markup supplied in the code. If the ARIA relationships are wrong, the widget may not work properly for screen reader users.

### Example: tablist and tabpanel

```html
<ul role="tablist">
  <li role="tab">Tab 1</li>
  <li role="tab">Tab 2</li>
  <li role="tab">Tab 3</li>
</ul>
<div role="tabpanel">Panel 1</div>
<div role="tabpanel">Panel 2</div>
<div role="tabpanel">Panel 3</div>
```
