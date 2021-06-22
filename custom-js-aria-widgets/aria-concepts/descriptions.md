# Description

## Using `aria-describedby`

The `aria-describedby` attribute is meant to be used to add extra, supplemental information about an element. Unlike `aria-labelledby` and `aria-label`, the `aria-describedby` attribute is not part of the [accessible name computation](https://www.w3.org/TR/accname-aam-1.1/#mapping_additional_nd_name). Instead it is part of the accessible description computation. In other words, don't use `aria-describedby` to give the element a name, label, or title. Instead, use it to describe or give supplemental information about the element.

If the element only needs an accessible name, don't use `aria-describedby` at all.

If an element has both a name and a description, screen readers first read the name of an element, then they read its description. In older versions of VoiceOver on OS X, the default setting was to delay the reading of the `aria-describedby` text by several seconds, making it highly unlikely that users would ever hear the `aria-describedby` text, because users would almost always move on past the element before the screen reader read the `aria-describedby` text. Thankfully, Apple has change the default setting to eliminate this delay. Users may still choose to implement the delay themselves by changing the settings, but that is outside of the developer's control.

## If the `aria-describedby` text is critical, it MUST be available to sighted users, and MUST be available in the document context (not just when the focus is on the element with the `aria-describedby` attribute) as text readable by screen readers.

### Example: Extra information about a form field is given via `aria-describedby`

```html
<label for="newPassword">Choose a new password:</label> 
<input type="password" id="newPassword" aria-describedby="pwdInfo"> 
<span id="pwdInfo">Minimum 8 characters, with both letters and numerals</span>
```

## Support for `aria-describedby`

Generally speaking, the following conditions must be met to ensure screen readers will read the `aria-describedby` text:

The element must have a semantic role. Most screen readers will not read `aria-describedby` text on `<span>` or `<div>` elements.

In many cases, the item must be a naturally focusable element (e.g. links, buttons, form elements).
The likelihood of the `aria-describedby` being supported is better in the case of items that typically can have accessible names such as images and tables.

Elements like paragraphs, headings, list items, lists, and so on typically are just considered text strings rather than items with accessible names, so most screen readers don't support `aria-describedby` on them.