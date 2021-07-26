# Test Form Validation

## Overview

Feedback after completing a form must be conveyed to both assistive technology users as well as to users who do not use assistive technology. Users need to know when they've successfully submitted a form, or if there are errors they need to fix before they can submit a form.

When testing for form validation, it is important to determine that both success messages and error messages are properly communicated to diverse users.

## Testing Methodology for Form Validation

### Error Messages

When a user makes an error in a form, feedback needs to be provided immediately. Users need to know that errors occurred and where those errors are within the form. Both of these components not only need to be visible to sighted users, but assistive technology users also need to be able to access this information.

There are a number of ways that error messages can be delivered to users. Some methods include providing an error summary that lists the number and type of errors, while other methods involve moving the focus to the first error in the form to allow users to move through the form and correct the errors. While design methods may differ, what is important is that feedback is delivered immediately, and that it is visible, meaningful, and accessible.

To test error messages:

- Locate a form on the web page.
- Do not fully complete the form, especially fields that are required or require special formatting (make mistakes on purpose).
- Submit the form.
- Check that feedback regarding errors is provided immediately after submission, this may include:
  - An error summary
  - Error messages for specific form elements that are next to the form elements
- Make sure that error messages are informative and actionable (users should know what to do to fix the error).

To test with a screen reader:

- Repeat Steps 1 through 3 above using a screen reader.
- Check that feedback is rendered by the screen reader immediately after submission.
  - A global error summary may be provided
  - Note: It is a best practice to ensure a method is provided to quickly access errors in the form in the error summary (e.g., a link to go to the first error in the form)
- Or focus may be shifted to first form element with an error
- Navigate to all the form elements with specific errors and make sure the error messages for those particular form elements are conveyed through the screen reader.

#### Example: Error message that is visible and programmatically associated

For the form input below, the error message is visible and exposed to screen readers through the use of `aria-describedby`.

```html
<div class="error">
  <span
    class="fa fa-exclamation-triangle"
    role="img"
    aria-label="Error: "
  ></span>
  <span id="errorMsg">Please Enter a Name for This Contact Person</span>
</div>
<p>
  <label for="name">Name: </label><br />
  <input
    type="text"
    name="name"
    id="name"
    aria-invalid="true"
    aria-describedby="errorMsg"
  />
</p>
```

##### Important

Some forms trigger error messages as users tab through the form or move away from a form element before filling it out. It is not recommended to tie error messages to these events, because screen reader users like to explore a form before filling the form out. If they explore the form and trigger error messages, they may encounter the error messages as they complete the form for the first time.

### Success Messages

When success messages are provided, they need to be visible to users who can see and exposed through assistive technologies.

To test success messages:

- Locate a form on the web page.
- Complete the form based on the instructions, if provided (see Test Form Labels and Instructions to evaluate the quality of instructions).
- Submit the form.
- Check that a success message is provided immediately after submission. The success message should be visible and have meaning (e.g., "Your form has been successfully submitted.").

To test with a screen reader:

- Repeat Steps 1 through 3 using a screen reader.
- Check that the screen reader conveys the message immediately after form submission.

### Mobile Web

Using either VoiceOver (iOS) or Talkback (Android):

- Locate a form on the web page.
- For success messages, complete the form without any mistakes. For error messages, make mistakes intentionally in the form, including not completing required fields and entering incorrect formatting in form fields with a formatting requirement.
- Submit the form.
- Check that success and errors messages are not only visible but also exposed to the mobile screen reader. For errors on particular fields, place the focus in the fields and make sure the error message for each of those fields is rendered by the screen reader.
