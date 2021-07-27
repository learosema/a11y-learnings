# Form inputs type="image"

## Form inputs with type="image" MUST have alternative text.

In order for alternative text to be programmatically determinable for an input with type="image", you must use the alt attribute on the input element.

```html
<input type="image" name="submit" src="submit-button.png" alt="Submit" />
```

## The alternative text for form inputs with type="image" MUST accurately convey the purpose or result of the input action.

The alternative text for an image input should describe the function of the input, not visual characteristics of the image.

## The length of the alternative text for inputs with type="image" SHOULD be concise (no more than about 150 characters).

Note: There is no technical limit nor policy restriction on the length of alt text, but alt text is not as usable as regular text for several reasons:

- Screen reader users cannot resume where they left off if they pause while in the middle of reading alt text.
- Screen reader users cannot navigate the text (e.g. by word, character, etc.).
- Some older screen readers do not read the full length of the alt text.
