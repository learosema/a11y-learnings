# Visual Customizability

## Fonts SHOULD be user-customizable.

To achieve user-customizability, text should be in regular HTML format, not in images. Regular text in the HTML document can be customized by users in terms of:

- Color (of the text and/or background)
- Size
- Font
- Font variations (underline, italic, bold, etc.)
- Line spacing
- Paragraph spacing
- Other visual characteristics

There are two main groups of people who would be interested in text customization:

- Users with low vision who often need large, high contrast text
- Users with reading disabilities who may need increased line spacing, paragraph spacing, or even custom fonts, such as fonts designed to be more easily readable for people with dyslexia (eg. [Dyslexie Font](https://www.dyslexiefont.com/), [Open Dyslexic Font](http://opendyslexic.org/), [Lexie Readable Font](http://www.k-type.com/fonts/lexie-readable/), and others).

Text embedded in images cannot be customized, so embedded text should be avoided if at all possible. 

If text must be embedded in an image, the vector-based SVG format has the advantage that it maintains its visual crispness and legibility when magnified. Text in raster-based formats — such as jpg, png, and gif — become pixelated and blocky when magnified, making them harder to read.

