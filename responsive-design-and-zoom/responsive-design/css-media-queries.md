# CSS Media Queries

## Specifying Layout Width

When paired with a viewport meta tag (discussed in the "Allowing Mobile Zoom" section of this course), CSS Media queries allow us to create styles that work across many different sizes of devices, all the way from the tiny screens of watches to the enormous screens used by many advanced (or just wealthy) desktop users. The basic idea is to create different sets of styles for different sizes of viewports, and to use the media query to match the sets of styles with the appropriate device sizes.

Media queries can be paired with several kinds of media types, logical operators, and other attributes.

### Example


#### Within the Same Style Sheet

The following example shows three sets of styles within a single style sheet. One set is for small devices (such as phones), one set is for medium-size devices (such as tablets), and one set is for large devices.

```css
@media (max-width: 700px) {
     /* small device styles go here */
}

@media (max-width: 1060px) {
     /* medium size device styles go here */
}

@media (min-width: 1061px) {
     /* large device styles go here */
}
```

#### In CSS Links

The following example shows the same media query sizes, but within CSS links, rather than within the same style sheet.

```html
<link rel="stylesheet" media="(max-width: 700px)" href="small.css" />
<link rel="stylesheet" media="(max-width: 1060px)" href="medium.css" />
<link rel="stylesheet" media="(min-width: 1061px)" href="large.css" />
```

## Media types

Media Types
Media types available for media queries include:

- all: for all media types and devices
- print: for printers
- screen: for computer screens, including tablets, phones, etc.
- speech: for screen readers
- embossed: for braille printers

Other media types are either deprecated or much less commonly used.

## Media Features

A more complete list of the media features supported in media queries includes the following:

- color, min-color, max-color: The number of bits per color component. A grayscale device would be 0.
- color-index, min-color-index, max-color-index: The number of colors in the color lookup table for the device, e.g. 128, 256, etc.
- aspect-ratio, min-aspect-ratio, max-aspect-ratio: The ratio of the viewport, with horizontal listed first, then vertical, e.g. 1/1, 2/1, etc.
- device-aspect-ratio: The ratio of the screen, with horizontal listed first, then vertical, e.g. 16/9.
- device-height: The height of the screen (not just the height of the rendering area)
- device-width: The width of the screen (not just the width of the rendering area)
- grid: Whether the device is grid-based, such as a TTY; allowed values: 1 or 0
- height, min-height, max-height: The height of the rendering area (the screen may be larger)
- monochrome, min-monochrome, max-monochrome: The number of bits per pixel
- orientation: landscape or portrait
- resolution, min-resolution, max-resolution: The pixel density of the device, specified in dpi or ppx
- scan: Allowed values: progressive or interlace
- width, min-width, max-width: The width of the rendering area (the screen may be larger)

## Combining Media Types and Features with Logical Operators

It is possible to create styles for very specific situations using logical operators in combination with media types and features.

### Complex Media Query Examples

```css
@media print and (min-resolution: 300dpi) { ... }
@media all and (max-width: 500), all and (color) { ... }
@media screen and (device-aspect-ratio: 16/9) { ... }
```