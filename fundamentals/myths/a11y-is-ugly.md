# Myth: Accessibility is ugly

## Truth: Accessible web site can be stunningly beautiful, or not

- Designs for people with disabilities can be just as beautiful (or as ugly) as designs for anyone else.

### Most web accessibility features are invisible

- alt text for images: invisible and only available to screen readers and other assistive technologies
- Labels for form elements: invisible (at lease the `<label>` tag itself is visible)
- Headings: you can style them with CSS as you like
- Table headers: The code to designate a header cell in a table (`<th>`) is invisible. Header cells are have bold centered text, but you can style them with CSS as you like
- Lists: alter the formatting by grouping the items by bullets or numbers, but you can style them with CSS as you like
- Language attribute: doesn't affect the visual look
- Keyboard Accessibility: doesn't affect the visual look
- Reading Order: Invisible
- Captions: if you use closed captions, the captions won't appear in the video for people who don't turn them on
- If you use closed audio descriptions, people won't hear them unless they turn them on.
- ARIA markup makes interactive JavaScript widgets more accessible to assistive technologies, without changing the visual appearance

A few a11y fixes do alter the appearance:

- Color contrast
- Links to skip navigation (one common workaround: make the link invisible until users tab to it)
- Cognitive disabilities (needs simplification of text, ui, etc)
