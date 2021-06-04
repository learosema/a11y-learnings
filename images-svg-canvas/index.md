# Images, SVG, and Canvas

## Every non-text element requires a text alternative

People who are blind do not access images directly. They listen to their screen readers read the alternative text that the developer or content creator provided for the image. In the case of users who are deafblind, the text is converted to refreshable braille characters that they feel with their fingers.

The techniques for supplying alternative text vary, depending on whether the image is presented in the `<img>` element, via SVG markup, via the HTML 5 `<canvas>` element, or via some other method. But the concept is the same: The alternative text must be meaningful and must serve as an effective substitute for the image in a way that makes sense to users who are blind.

Other kinds of content usually require alternative representations too, such as:

- Video (which requires captions, a transcript, and which may require audio descriptions)
- Audio (which requires a transcript, at a minimum)
- Plug-ins (which require effective use of their respective accessibility APIs)
- Documents (e.g. Word, PowerPoint, PDF, etc., which also require effective use of their respective APIs)

Often it is best to also create an HTML-based alternative version of non-HTML content, because HTML usually offers the greatest potential for accessibility across the greatest diversity of devices.
