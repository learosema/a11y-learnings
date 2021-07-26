# Test Form Labels and Instructions

## Overview

Clear labels and clear instructions are important for forms accessibility. Form fields and other form controls usually have visible labels, such as "E-mail Address:" as the label for a text field. When these labels are marked up correctly, people can interact with a form using only the keyboard, using voice input, and using screen readers.

Also, when proper markup is used, the label itself may become selectable, which enables a person who has difficulty clicking on small radio buttons or checkboxes to click anywhere on the label text. When clear instructions for the entire form, groups of form elements, and individual form elements are marked up correctly, it may prevent both assistive technology users and non-assistive technology users from generating errors while completing the form.

### Testing Methodology for Form Labels

Look for any forms on the web page. A form can be a single text field, such as Search, or can be a complex form with text fields, radio buttons, checkboxes, drop-down lists, and buttons.

It is important that labels are marked up properly in order to be available to assistive technologies. Automated tests may help you identify if labels are correctly associated with form fields and confirm that unique IDs are used throughout the web page.

If IDs aren't unique, especially in forms, labels may not be associated correctly with the intended form field. Manual testing is used to validate the positioning and effectiveness of form labels.

### Individual Form Elements

When evaluating labels for individual form elements, check for the following:

- The label for the form element is visible to sighted users and near its form element.
- Placeholders alone aren't used as labels. Since placeholders disappear once a user enters information, placeholders are not sufficient as visible labels.
- The label is exposed to assistive technologies. To check for this, use a screen reader and place the focus on the form input (text field, radio button, etc.). The label associated with the form input should be rendered by the screen reader. If not, the label is not marked up properly.
- The label properly names or conveys the purpose of the form element. Users should know what to do when they encounter the label.
- When an image or icon is used as a label, check for a proper text alternative using a screen reader. The text alternative should be rendered when focus is placed on the form input.

#### Example

When focus is placed inside the field, the screen reader will render the field's label.

```
<!-- label associated with text field -->
<label for="firstName">First name</label>
<input type="text" name="firstName" id="firstName">
```

### Grouped form elements

For form elements that are related to each other, they not only need individual labels, but they also need a group label to properly communicate all the context for the related form elements. Groups of radio buttons or checkboxes almost always have a group label.

When evaluating a form, look for form elements are that related to each other (e.g., contact information, billing address) and check for the following:

1. A group label for related form elements is visible to sighted users and near the form elements it labels.
2. The group label is exposed to assistive technologies. Use a screen reader and place the focus within the form grouping. When focus is placed on the first form element in the group, both the group label and the individual label for the form element should be rendered by the screen reader. If the group label isn't rendered, then it is not properly marked up.
3. The group label properly names or conveys the purpose of the form grouping.

#### Example

The group label needs to be programmatically associated so users can make sense of the information they need to provide for the set of form fields. This can be done via a `fieldset`.

When screen reader users navigate into the group below, the group label will be rendered through the screen reader.

```html
<fieldset>
  <legend><strong>Contact Information</strong></legend>
  <p><label for="name">Name: </label><input type="text" id="name" /></p>
  <p><label for="phone">Phone: </label><input type="text" id="phone" /></p>
  <p><label for="email">Email: </label><input type="text" id="email" /></p>
</fieldset>
```

### Testing Methodology for Form Instructions

#### Entire Form and Grouped Sections of Form

If instructions are needed for a user to successfully complete an entire form or a grouped section of a form, then those instructions need to be available to all users.

To check for the accessibility of form instructions for an entire form or group of form elements, look for the following:

- The instructions for the form or form group are visible and appear before users interact with form elements.
- The instructions are available to assistive technologies (Check that a screen reader renders instructions to users).
- Instructions for form groups are associated programmatically with their specific form elements.
  - To check this, use a screen reader and tab into the form grouping. The screen reader should render instructions to users either when they tab into the grouping (`<legend>`) or when they tab to a form element in the grouping (`aria-describedby`).
- The instructions are meaningful and actionable. Users should know exactly what to do after reading the instructions.
- Instructions do not rely on sensory characteristics like color alone. For example, instructions should not say fields outlined in red are required.

##### Example

The ARIA attribute `aria-describedby` has been used to ensure that when a screen reader user navigates into the password fields, they will know what the instructions are for those fields.

```html
<fieldset>
  <legend>Create Account</legend>
  <p>
    <label for="username2">Username: </label>
    <input type="text" id="username2" />
  </p>
  <p id="passwordInstructions">Password fields must match</p>
  <p>
    <label for="password2">Password: </label>
    <input
      type="password"
      id="password2"
      aria-describedby="passwordInstructions"
    />
  </p>
  <p>
    <label for="password22-">Re-enter password: </label>
    <input
      type="password"
      id="password22-"
      aria-describedby="passwordInstructions"
    />
  </p>
</fieldset>
```

#### Individual Form Elements

Individual form elements may have specific instructions, for example, if the field is required or special formatting is needed in the form field. Specific instructions for form elements must be available to assistive technology users as well as to people who don't use assistive technologies.

When testing the accessibility of instructions for specific form elements:

- Check that instructions are visible and near the form element they describe.
- Check that instructions are available to assistive technology users. Use a screen reader and place focus on the form element. The screen reader should render instructions to users when focus is placed on the form element.
- Make sure instructions are specific and meaningful. Users should know whether a field is required or what kind of formatting is needed to complete the form field.
- Make sure instructions do not rely on sensory characteristics such as using color alone to convey a required field.

##### Example

The ARIA attribute `aria-describedby` is used for the input field below to associate the instructions with the form field. So, now when focus is placed in the field, the instructions will be conveyed through a screen reader.

```html
<label for="date2"><strong role="presentation">Date:</strong></label>
<input type="text" name="date2" id="date2" aria-describedby="dateFormat" />
<span id="dateFormat">(MM/DD/YYYY)</span>
```

#### Mobile Web

- Check that instructions and form labels are visible to users as they navigate the form.
- Using either VoiceOver (iOS) or Talkback (Android):
  - Check that instructions for the entire form and grouped sections are visible and conveyed through the screen reader.
  - For individual form elements, place focus in or on the form element. Check that the label is rendered through the screen reader and that any specific instructions for the element are communicated as well.
