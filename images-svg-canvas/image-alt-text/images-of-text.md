# Images of text

## An image MUST NOT include informative text if an equivalent visual presentation of the text can be rendered using real text.

Wherever possible, use text instead of images of text, except when the image is decorative in nature, or the text in the image is essential.

### Exception: Logo text in image

There is an exception in WCAG which allows for the use of text in images when the image itself is decorative in nature or the text in the image is essential. A typical example of this is a company logo. Text in an image is permissible when it is part of a logo. Remember to include alt text that states the text in the logo.

```html
<img src="deque_logo.png" width="165" height="59" alt="Deque">
```

## Images MUST NOT include informative text, unless the text is essential (such as a logo), or the font, size, color, and background are customizable.

When images that contain text have a proper alternative description, the text will be accessible to screen reader users; however, people with low vision cannot customize the text in the images to read the text. There are some ways that text in images can be preserved as real text, making it available to assistive technology users. Text in an image like SVG remains as real text, meaning that screen reader users can access it and low vision users can customize it.

### Example: Customizable text in SVG image

In this example, a screen reader will render the text "Real text here". In addition, since the graphic is SVG, it can be easily scaled, benefiting those with low vision who may utilize screen resizing. Keep in mind that the contrast between text and background must be sufficient.

```html
<svg width="150" height="150" role="img">
  <rect width="150" height="150" fill="#0000FF" stroke="#000" stroke-width="1"/>
  <text id="text" x="75" y="85" font-size="1em" 
     text-anchor="middle" fill="#FFFFFF">Real text here</text>
</svg>
```
