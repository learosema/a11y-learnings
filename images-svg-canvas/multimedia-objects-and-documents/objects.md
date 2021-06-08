# Other objects

## All `<object>` elements MUST have alternative text.

The `<object>` element is less common than it once was, but it can be used to display content like images, PDF files, videos, and audio, among other things. 

The `<object>` element needs a brief alternative text, along the same lines as the alt attribute for images, but there is no alt attribute allowed on the `<object>` element. Instead, use aria-label (to add invisible alternative text for screen readers) or aria-labelledby to refer to text elsewhere on the page.

As with all alternative text, ensure it is:

- meaningful (conveying the purpose of the `<object>`)
- concise (no more than about 150 characters).

If it takes more than 150 characters to describe the `<object>`, consider one of the following options:

- Add a long description, using the same techniques available for image long descriptions, OR
- Create an HTML-based equivalent of all of the content and functionality of the `<object>`. This is the best option when the `<object>` is an interactive web application.

## Example: `aria-label`

```html
<object width="500" height="500" data="chemistry-titration-experiment.png"
   aria-label="Steps for performing a chemistry titration experiment">
</object>
```

Of course, just saying what the `<object>` is does not make it accessible. It only allows the user to know what it is. To truly make the steps of a chemistry titration experiment accessible, you would need to follow the other accessibility principles related to image accessibility, such as including a copy of the written steps in text-based HTML format.

## Example: `aria-labelledby`

```html
<h2 id="titration">Steps for performing a chemistry titration experiment"</h2>
<object width="500" height="500" data="chemistry-titration-experiment.png"
   aria-labelledby="titration">
</object>
```
