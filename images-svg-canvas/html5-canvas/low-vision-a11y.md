# Low Vision Accessibility

## All `<canvas>` elements SHOULD have a background fill.

If a `<canvas>` element does not have a background fill color, the background color may change when users change their color or contrast preferences, such as when using Windows High Contrast Mode.

One of the most common background colors in Windows High Contrast Mode is black, so the background of the canvas image will change to black if there is no background fill color.

## If text is required in a graphic, it MAY be more appropriate to use SVG instead of `<canvas>`.

The `<canvas>` element renders graphics as raster images, similar to jpg, gif, and png images. This means that the images will look blockier or more pixelated when magnified. This problem is most pronounced when text is included within the image. Text inside `<canvas>` elements is not as easy to read as regular text in the document. When text is required in an image — such as in the charts shown in the examples on this page — the best practice overall would be to create the charts as SVG graphics instead of `<canvas>` graphics. SVG graphics are vector-based, so they will scale infinitely and always be easy to read.