# Visibility of Labels

## Labels MUST be visible.

Visible labels benefit all users. When form fields do not have labels that are meaningful and visible to all users, at all times, users might have to guess or infer what goes in them. This often happens when placeholder text is used alone to visually label text fields or dropdown lists are labeled by the first selection.

### Good example

This form uses a clear visual label for its input that sighted users can understand. But it also maintains understandability with use of the invisible aria-label to assist non-sighted users with specifics that aren't necessary for sighted users.

```html
<p>
  <label for="ssn1">Social Security Number:</label> 
  <input type="text" size="3" maxlength="3" id="ssn1" aria-label="Social Security Number first three digits"> -
  <input type="text" size="2" maxlength="2" aria-label="middle two digits"> -
  <input type="text" size="4" maxlength="4" aria-label="last four digits">
</p>
```

## For user interface components with labels that include text or images of text, the name MUST contain the text that is presented visually.

The label for a control that a user sees on a page must match the accessible name of that control recognized by assistive technology. If these names do not match, then users who use speech to control their screen may have difficulty activating controls on the screen.

Assistive technologies construct accessible names using an algorithm that adds together various pieces of information about the element. These include the text that appears on the element, any form labels, and any aria-label or aria-labelledby attributes. Most of the time, failures of this success criterion will be paired with a failure of another success criterion, but here are a couple of things to keep in mind:

1. You should avoid using text in an image, but if you do use text in an image as a button, make sure the alt text matches the image text.
2. `aria-label` and `aria-labelledby` override other information about the element when the assistive technology creates an accessible name. This means that adding an aria-label does not add additional information to the name, it simply replaces the other information. Making sure that the aria-label or aria-labelledby attributes contain what the user sees is important, because those attributes become the entire accessible name.