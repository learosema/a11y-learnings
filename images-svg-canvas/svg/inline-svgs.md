# Inline SVGs

## Overview

A major advantage of embedding the `<svg>` element inline with HTML, instead of utilizing the `<img>` tag and referencing the SVG file as the source, is that JavaScript and CSS can be applied to the `<svg>` contents to animate or manipulate the image.

There are a few downsides to this method:

- Even though SVG images have been around for many years, assistive technology support is not consistent. The rules provided below provide the best experience across the widest range of assistive technologies.
- The increased embedded code will also result in an increased file size.
- The inline SVG cannot be cached.
- If the image is used in multiple places, maintaining inline SVG code becomes more complicated.

## All `<svg>` elements MUST be set to role="img".

To ensure the widest range of assistive technologies recognizes the SVG as an image, add role="img" to the `<svg>` element.

## All informative or actionable `<svg>` elements MUST have meaningful alternative text (via the `<title>` element).

When adding an SVG element inline, it is important to add concise, meaningful alternative text via the `<title>` element of the `<svg>`. The content of the alternative text is determined the same way it is for a regular image, in the sense that it must describe the purpose or meaning of the image.

The `<title>` needs to be the first-child of its parent element. This is pertinent because an `<svg>` element can have multiple titles, depending on whether it contains multiple containers (or groupings) of graphical elements.

## The alternative text (`<title>`) of an `<svg>` element MUST be programmatically associated with the `<svg>` element via aria-labelledby.

While a `<title>` provides the equivalent of alternative text for SVG, the unfortunate reality is that not all browsers expose this information through the Accessible API. Furthermore, not all screen readers actually make use of it. 

However, exposure to screen readers can be drastically increased by simply adding the aria-labelledby attribute in the `<svg>` tag and then tying it directly to the `<title>`.

Most modern browsers offer full support of ARIA so by adding the aria-labelledby attribute, the net effect will be that the browsers which currently don't expose the information through the `<title>` natively, will now make use of the information based on the ARIA attribute.

#### Example

```html
<svg role="img" aria-labelledby="widgetSales">
  <title id="widgetSales">Total Widgets Purchased during 2016</title>
</svg>
```

## All text within the image that needs to be spoken by a screen reader MUST be associated with the `<svg>` element using aria-labelledby.

If an SVG contains text that must be spoken by a screen reader and is not already included in the `<title>` or `<desc>` elements, it must be associated with the `<svg>` element using aria-labelledby.

### Example

```html
<svg role="img" 
<!-- note that aria-labelledby references the IDs of elements. Screen readers read the text inside those elements, not the IDs themselves, which are used only to identify the elements. -->

   aria-labelledby="title desc jan feb mar apr may jun jul aug sep oct nov dec"> 
<title id="title">Total Widgets Purchased during 2016</title>
  <desc id="desc">
  The graph displays the total number of widgets purchased from The ABC Store
  during 2016, displayed by month.
  </desc>
  ... (a section of markup was omitted here for brevity)
  <g id="jan" class="bar labels x-labels">
    <rect x="25" y="195" width="33" height="45" fill="#111"></rect>
   <text x="32" y="260" fill="#000">Jan.</text>
   <text x="33" y="220" fill="#fff">45</text>
  </g> 
  <g id="feb"  class="bar labels x-labels">
    <rect x="62" y="160" width="33" height="80" fill="#111"></rect>
   <text x="70" y="260" fill="#000" >Feb.</text>
   <text x="71" y="220" fill="#fff">80</text>
  </g> 
  <g id="mar"  class="bar labels x-labels">
    <rect x="99" y="140" width="33" height="100" fill="#111"></rect>
   <text x="107" y="260" fill="#000" >Mar.</text>
   <text x="103" y="220" fill="#fff">100</text>
  </g> 
  ... (partial code sample)
</svg>
```

## The total number of characters of alt text associated with the `<svg>` element SHOULD NOT exceed 150 characters.

As discussed previously, there is no technical limit nor policy restriction on the length of alternative text, but the SVG's alternative text is not as usable as regular text for several reasons:

- Screen readers read the entire string of text at one time, and users cannot resume where they left off if they pause while in the middle of reading the alternative text.
- Screen reader users cannot navigate the text (e.g. by word, character, etc.).
- The text that is associated with the SVG, including the `<title>`, `<desc>`, and each necessary piece of text, should not exceed about 150 characters. If more text is required, consider using one of the techniques for complex images that makes the content available to all users:

1. Within the context of the HTML document itself.
2. With a button that expands a collapsed region that contains the long description.
3. With a button to open a dialog that contains the long description.
4. With a link to a long description via a normal link text.
