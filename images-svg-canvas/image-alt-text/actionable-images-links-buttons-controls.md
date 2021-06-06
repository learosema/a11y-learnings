# Actionable Images (Links, Buttons, Controls)

## All actionable images (e.g., links, buttons, controls) MUST have alternative text.

Ensure that alternative text for actionable graphics clearly describes the destination, purpose, function, or action. Do not include "link to" in the alt text since screen readers will announce that the image is a "link graphic" before announcing the alt text.

WCAG 2.1 — 1.1.1 says that "If non-text content is a control or accepts user input, then it has a name that describes its purpose." In the case of images used as controls, the alternative text should describe the action of the control, not the image itself.

### Good Example: Image Used as a Link Has Useful Alt Text

```html
<a href="#"><img src="home.png" alt="Home" width="113"></a>
```

## The alternative text for actionable images MUST be meaningful (accurately conveying the purpose or result of the action).
For actionable images, it is important that the alternative text describes the purpose or the functionality of the image. For instance, the alternative text for an image that is a link will describe the link destination, not the shape or other visual characteristics of the image. The alternative text for an image that is a button will describe the function of the button (e.g., a "Submit" button).

## Alternative text SHOULD NOT include words that identify the element as a link, graphic, or image.

Screen readers announce "image" or "graphic" as they read the alternative text for an img, AND they announce "link" as well, when the image is inside an anchor tag. Therefore, including words such as "link to", "image of", or "graphic of" in the alternative text is unnecessary. The alternative text should describe the destination or action of the link.

The length of the alternative text for actionable images SHOULD be concise (no more than about 150 characters).
There is no technical limit nor policy restriction on the length of alt text, but alt text is not as usable as regular text for several reasons:

- Screen reader users cannot resume where they left off if they pause while in the middle of reading alt text.
- Screen reader users cannot navigate the text (e.g. by word, character, etc.).
- Some older screen readers do not read the full length of the alt text.