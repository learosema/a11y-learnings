# Responsive Design and Zoom: Summary & Checklist

Even though responsive design was invented primarily for small screens and mobile devices, responsive design greatly benefits people with low vision who need to zoom in on content.

Zooming in reduces the amount of screen real estate available, creating conditions essentially identical to the small screens of small mobile devices.

When the screen real estate is limited, it's best if the design can adapt by becoming simpler and "slimmer," fitting in a single column, rather than in two or more columns.

Text should reflow to fit the smaller screen size, and horizontal scrolling should be eliminated, if possible. In short, the design should be optimized for viewing in mobile or zoom conditions.

## Responsive Design

-Forms SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Images SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Objects/plugins SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Tables SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Text SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-UI components SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Video elements SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.
-Features of the content MAY be simplified, reduced in size, or eliminated when magnified or when viewed on small viewports.
-Features of the interface SHOULD be simplified, reduced in size, or eliminated when magnified or when viewed on small viewports.

## Zoom

### Text resize/zoom:

-The page SHOULD be functional when only the text is magnified to 200% of its initial size.
-The page SHOULD be readable when only the text is magnified to 200% of its initial size.
-The spacing between letters, words, lines of text, and paragraphs MUST be adjustable without loss of content or functionality.

### Content reflow:

- Content MUST NOT require scrolling in two directions (both vertically and horizontally) — even when the viewport is set or zoomed to 320 CSS pixels wide (for vertically-scrolling content) or 256 CSS pixels high (for horizontally-scrolling content) — unless both scrolling directions are essential to the usage or meaning of the content.
- Mobile zoom: The page MUST allow users to zoom in on mobile devices.

### Magnification visual quality:

- Text SHOULD magnify losslessly, or with minimal visual degradation, to retain readability.
- Icons and graphics SHOULD magnify losslessly, or with minimal visual degradation.

## Orientation

Content MUST NOT restrict its view and operation to a single display orientation, such as portrait or landscape, unless a specific display orientation is essential.

## Target Size

The click/touch target size SHOULD be large enough to facilitate easy use with a finger, without risking activating an adjacent link or button.
