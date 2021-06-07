# Text in SVGs

## Text within <svg> elements SHOULD be eliminated OR SHOULD be kept to a minimum.

The good news about text within <svg> elements is that it remains crisp and highly readable, even when magnified, because of the vector format of SVG images, which is great for people with low vision.

The bad news is that when used as alternative text, screen readers will treat all of the <text> elements as one continuous string of text, which can be confusing if the <text> elements are meant to identify separate parts of the image, or if they are not meant to be read together as a single string of text.

The recommendation is to limit the amount of text in an <svg> element to only the essential items or eliminate it altogether. If possible, place the text outside of the <svg> element, in the regular flow of the HTML document.

## All informative <text> elements inside <svg> elements MUST be referenced in the alternative text of the <svg> element, or in a long description.

If you don't add <title> or role="img" to an <svg> element, some screen readers will ignore the fact that it is <svg> and instead just read the text within it. That sounds like a good thing, and in some ways, it is, but there are drawbacks.

Screen reader behavior is not uniform across the different brands, so the end result is not consistently accessible that way.

Also, the <title> element is essentially a requirement, but won't be recognized by all screen readers unless you also add role="img". Once you add both <title> and role="img", the behavior of screen readers changes. Instead of treating the <text> element as text, screen readers treat the <svg> element as an image, and they ignore the <text> element inside.

In essence, there are drawbacks no matter what you do. Until screen readers get more consistent about how they handle <svg> elements, the recommendation is to ensure that all informative text within the <svg> element is referenced via `aria-labelledby`.

### Note

If some of the text in the <svg> element would not make sense as part of the alternative text, do not reference it via aria-labelledby.

### Example

```html
<svg width="200" height="163" role="img" aria-labelledby="circle-alt svg-text">
  <title id="circle-alt">A dark blue circle with text inside</title>
  <circle cx="81" cy="85" r="75" fill="#00a" stroke="#000" stroke-width="1"/>
  <text id="svg-text" x="81" y="85" font-size="14px" text-anchor="middle" fill="#fff">
      I am text in a circle
  </text>
</svg>
```
