#  CSS Background Images

## Purely decorative or redundant CSS images SHOULD NOT have a text alternative in the HTML content.

Images that are purely for decoration or are already described in the text next to the image do not need to be described through alternative text. Decorative images do not communicate useful information to the user, so no alt text is necessary. As for images described in the text document, if you provide that same information through an image's alt text, a screen reader user will hear the information twice, potentially impacting the usability of the web page.

## The alternative text for informative or actionable CSS images MUST be available as programmatically determinable text in the HTML content.

Whenever possible, it is best to avoid placing informative and actionable images in CSS. However, if it is necessary to do so, you can add alternative text to informative and actionable CSS images. The following examples show how alternative text can be programmatically available by using the CSS clip method or by using the aria-label attribute.

### Example

The Facebook icon is a background image, but the link has an aria-label associated with it explaining what the link is for.

```html
<a href="http://www.facebook.com/dequesystems" class="fb"
  aria-label="Deque's Facebook page"></a>
```

### Example: visually hidden text

```html
<a href="https://www.facebook.com/dequeuniversity" class="facebook_icon">
  <span class="visually-hidden">Deque University Facebook page</span>
</a>
```

## The alternative text (in the HTML content) for informative or actionable CSS images MUST adequately and accurately describe the purpose of the image.

As with standard images, the alternative text provided for informative and actionable CSS images must describe the intent, purpose, or functionality of the image.
