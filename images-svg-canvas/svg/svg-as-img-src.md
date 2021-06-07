# SVG as img src

## Overview

### Note

There are multiple ways to embed an SVG into a web page:

1. Utilize the `<img>` tag and reference the SVG file as the source (e.g. <img src="SVGFile.svg" alt="some alt text">).
2. Embed the SVG directly (inline) into your existing HTML code, using the `<svg>` element.
3. Embed the SVG in an `<iframe>` or `<embed>` tag, or referenced as the data attribute through an `<object>`.

From an accessibility standpoint, the most reliable methods are #1 and #2: utilizing the `<img>` tag or embedding the SVG in the HTML using the `<svg>` element. The results of using `<iframe>` or `<object>` elements are very poorly supported by assistive technologies.


For basic, uncomplicated images, utilizing the `<img>` tag and referencing the SVG file as the source is a straightforward way to go. Benefits of this method include:

The HTML file size will be smaller than embedding the `<svg>` element inline.
The image can be cached by the browser.
If you are using the SVG in multiple places, one image file makes maintenance simpler.
There are a few downsides to this method:

JavaScript and CSS cannot be applied to the `<svg>` contents to animate or manipulate images.
The SVG source is not directly available in the DOM and may provide less predictable results for assistive technologies if the image is complex.

## All SVG `<img>` elements SHOULD be set to role="img".

To ensure the widest range of assistive technologies recognizes the SVG as an image, add role="img" to the `<img>` element.

```html
<img src="somesvg.svg" role="img" alt="Alt text">
```

## All SVG `<img>` elements MUST have meaningful, concise alternative text (via alt, aria-label, or aria-labelledby).

When adding an SVG element via an `<img>` element, it is important to add concise, meaningful alternative text via alt, aria-label, or aria-labelledby attributes within the `<img>` element. The content of the alternative text is determined the same way it is for any `<img>` element, in the sense that the purpose or meaning of the element should be described by the alternative text.

```html
<img src="somesvg.svg" role="img" alt="a concise description of the image"> 
```