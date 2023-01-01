# Forms

## Form Controls Need Labels

### Form Labels

Every form element needs a label, and that label must be associated explicitly with the form element in the markup.

Users need to know what form elements are for. When users see a text input, they need to know if they should type in their name, or their phone number, or their email, or what kind of cereal they ate today for breakfast.

Without a label, users won't know what to do. Sighted users can see the text on the screen, so if everyone were sighted, all you would need to do is type the label next to the form control. The label could just say "Name" or "Email" or whatever is appropriate.

Not everyone is sighted though. You need to add a bit of extra markup for screen reader users to ensure that the screen reader will read the label with the form element. The most straightforward way to apply a label is to use the <label> tag.

## Good Example of a Form Input with a Label

The following form element has a text label associated with the text input using the <label> tag.

<label for="email">Email:</label> <input type="text" name="email" id="email">

When screen reader users tab to this form element, they will hear "Email, text input, blank" (the word "blank" means that there is no text in the text input yet). The markup is shown below.

```html
<label for="email">Email:</label> <input type="text" name="email" id="email">
```

Labels for forms can get quite complex. Deque's HTML and CSS Accessibility course goes into much more detail with regard to forms and form labeling.

## See also

- [briefs.video: What happened to text inputs?](https://briefs.video/videos/what-happened-to-text-inputs/)
