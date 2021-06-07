# Complex Alternative Text

## Complex <svg> images MUST have meaningful, concise alternative text AND MUST have a more complete long description.

Even if you've correctly associated visual labels with visual data in a graph or chart, blind users won’t be able to easily make sense of the graphics unless you provide a detailed text description of them. You could add all of the description to the short alternative text, but that is meant to be somewhat brief, no more than roughly 150 characters or so. If 150 characters or so is insufficient to describe an image, you must use another method.

There are several ways of providing a long description for SVG images:

1. Provide the long description in the context of the HTML document itself.
2. Provide a button that expands a collapsed region that contains the long description.
3. Provide a button to open a dialog that contains the long description.
4. Provide a link to a long description on another page via a normal link text.
5. Via the <desc> attribute within the <svg> element.

Ideally, the long description should be available to sighted and non-sighted users alike; therefore, options #1 - #4 above are strongly preferred.

## A <desc> element MUST be used to provide a detailed description of a complex <svg> if it is not provided in any other way.

In addition to the <title> which essentially serves as alternative text for the image, the <desc> element provides a way to fully describe the graphic. For simple images, the alt text nature of the <title> will probably suffice. But for more complex structures, the <desc> serves an equivalent purpose as the longdesc attribute does for a normal <img> element. However, the benefit in this case is that the description is provided as part of the image itself, whereas with a raster image, the longdesc attribute simply points to another location that contains the detailed description.

### Note

The <desc> element is only available to screen reader users and is, therefore, not the preferred method of providing a detailed description for an SVG image.

## The <desc> attribute of an <svg> element MUST be programmatically associated with the <svg> element (via aria-labelledby).

While the <desc> provides the ability to offer up a detailed description of an SVG image for assistive technology, the unfortunate reality is that not all browsers expose this information through the Accessible API. Furthermore, not all screen readers actually make use of it. 

, exposure to screen readers can be drastically increased by simply adding the aria-labelledby attribute in the <svg> tag and then tying it directly to the <desc> element's ID. 

Most modern browsers offer full support of ARIA so by adding the aria-labelledby attribute, the net effect will be that the browsers which currently don't expose the information through <desc> natively, will now make use of the information based on the ARIA attribute.

## The length of all associated alternative text (including <title> and <desc>) for the <svg> element SHOULD be concise (no more than about 150 characters).

Because both the name and description of an <svg> object must both be referenced with aria-labelledby (due to poor screen reader support for aria-describedby on <svg> objects), the total number of characters in the alternative text is the combination of all things referenced by the aria-labelledby attribute, including both the <title> and <desc> elements. If there are 100 characters in the <title> element, and 200 characters in the <desc> element, the total number of alternative text characters is 300, which is twice the maximum recommended amount.

As discussed previously, there is no technical limit nor policy restriction on the length of alternative text, but the alternative text is not as usable as regular text for several reasons:

- Screen readers read the entire string of text at one time, and users cannot resume where they left off if they pause while in the middle of reading the alternative text.
- Screen reader users cannot navigate the text (e.g. by word, character, etc.).

If more text is required to describe the image in a meaningful way, consider using one of the following techniques for complex images that makes the content available to all users:

1. Provide the long description in the context of the HTML document itself.
2. Provide a button that expands a collapsed region that contains the long description.
3. Provide a button to open a dialog that contains the long description.
4. Provide a link to a long description on another page via a normal link text.

