# Embedded SVGs

## An SVG object SHOULD NOT be embedded via `<object>` or `<iframe>`.

From an accessibility standpoint, the most reliable methods are: utilizing the `<img>` tag or embedding the SVG in the HTML using the `<svg>` element.

### Note

Since the results of using `<iframe>` or `<object>` elements are very poorly supported by assistive technologies, using these methods has a high probability of resulting in an image that is not accessible to assistive technology.
