# Tab Focusability

## Links, buttons, and interactive controls MUST be keyboard-focusable.

Keyboard users navigate through a web page using the Tab key. The Tab key moves the keyboard focus to each focusable element on a page. So, it is critical that all focusable elements on the page are able to receive keyboard focus.

When focusable elements do not receive keyboard focus, it is difficult—and nearly impossible—for keyboard users to activate and interact with those elements on the web page.

The following elements — whether they be native HTML elements, custom versions of native elements, or totally custom controls or widgets — must receive keyboard focus:

- links
- buttons
- inputs:
  - text inputs
  - image inputs
  - submit buttons
  - radio buttons
  - checkboxes
  - All other input types
- drop-down selection inputs
- textarea fields
- ARIA controls:
  - ARIA links
  - ARIA buttons
  - ARIA inputs
  - ARIA tabs
  - All other focusable custom ARIA controls
- All other focusable custom elements and widgets

# Example

If you use a custom link which is not an `<a>` tag, use `tabindex="0"` to make it focusable:

```html
<span role="link" tabindex="0" data-href="https://www.deque.com">Deque.com</span>
```

