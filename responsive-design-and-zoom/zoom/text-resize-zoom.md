# Text Resize/Zoom

## Text-only Zoom

Most browsers allow both full-page zoom and text-only zoom. For example, in Firefox you can choose View > Zoom > Zoom Text Only from the main menu.

With full-page zoom, everything magnifies proportionally. With text-only zoom, only the text magnifies, without expanding the layout elements, tables, images, videos, or any other part of the design.

Full-page zoom usually does not affect the design or layout. Text-only zoom can have a dramatic impact on the design and layout. It can be tricky to design in a way that allows text-only zoom, but designing with responsive design principles in mind can help.

## The page SHOULD be functional when only the text is magnified to 200% of its initial size.

### Bad example

When the text on this website in this example is zoomed to 200%, the links overlap, making them not only difficult to read, but difficult or impossible to use for navigation.

## The page SHOULD be readable when only the text is magnified to 200% of its initial size.

### Option 1: use `em` instead of `px`

The biggest barrier to effective text zoom is the use of pixels when specifying the dimensions of objects in a web layout. If you specify the width and height of a `<div>` as 100px and 200px, any content that is larger than those dimensions will spill out onto other areas of the web page. Or, if the designers use CSS properties like overflow:hidden, the extra text will be clipped and completely invisible when the text is zoomed.

One way to fix the problem is to assign a height and the vertical portion of the padding in em units, rather than pixels. The em unit is always relative to the font size, so it should enlarge in proportion to the size of the text.

### Option 2: no height assigned/ height: auto

Under some circumstances, the height may not be important. We can delete the height completely from the CSS and the content will always flow to fit the height. In this particular example, that leaves our two columns with unequal heights, which may not be a bad thing, depending on the design you have in mind. If matching heights are important, there may be other ways to style things to make them look right.

## The spacing between letters, words, lines of text, and paragraphs MUST be adjustable without loss of content or functionality.

Users sometimes modify text spacing with custom CSS to allow for better readability. This can be especially helpful to people with dyslexia. Ensure that no content or functionality is lost when text is adjusted to the following:

- Line height (line spacing) to at least 1.5 times the font size
- Spacing following paragraphs to at least 2 times the font size
- Letter spacing (tracking) to at least 0.12 times the font size
- Word spacing to at least 0.16 times the font size

These spacing requirements are not applicable for all written languages. For example, letter spacing is not applicable for languages written using logographs instead of letters, such as Chinese. Word spacing and line height, however, would still be applicable in this case.
