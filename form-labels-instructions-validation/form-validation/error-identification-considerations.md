# Error Identification Considerations

## Error feedback SHOULD be made available immediately after form submission (or after an equivalent event if there is no form submission event).

When users submit a form and there are errors on form inputs, users should be alerted immediately after form submission of those errors. If errors are not immediately identified, users may abandon completing the form altogether, especially screen reader users.

If screen reader users cannot detect errors immediately, the impression may be that the form is broken or doesn't work. Design Pattern 1, Design Pattern 2, and Design Pattern 3 in this section identify ways in which errors can be identified immediately to both sighted users and non-sighted users.

## Error feedback MUST be programmatically associated with the appropriate element.

Mistakes are bound to happen in forms, even when detailed and specific instructions are provided. When they do occur, though, especially with specific inputs, users must be made aware of those errors.

It is particularly important that when errors occur in specific form inputs that assistive technology users can access the error messages. Ensuring that error messages are programmatically associated with their corresponding input fields helps assistive technology users access that information and fix the error.

### Example

- use `aria-invalid` and `aria-describedby`to programmatically associate the error message with the input field

```html
<div class="error">
  <span class="fa fa-exclamation-triangle" role="img" aria-label="Error: "></span> 
  <span id="errorMsg">Please Enter a Name for This Contact Person</span>
</div>
<p>
  <label for="name">Name: </label><br>
  <input type="text" name="name" id="name" aria-invalid="true" aria-describedby="errorMsg">
</p>
```

## Error feedback MUST be programmatically determinable.

In order for assistive technologies like screen readers to access error messages, error messages either need to be composed as actual (real) text or text must be provided through an alternative like `alt`, `aria-label`, `aria-labelledby`, and `aria-describedby`. Without programmatically determinable text, it would be near impossible for assistive technologies to be able to render error messages to users.

## Error feedback MUST be meaningful.

When error messages are presented to users, they should be clear, accurate, and provide actionable information that allows users to fix the error properly. Give users correction cues within the error messages for specific form inputs, buttons, or other controls.

- Good: Email Address field cannot be blank
- Bad: Can't save subscriber due to error (it's unclear!)

## Error feedback MUST be visible.

Users who can see must also receive feedback if they commit any errors on specific form inputs. So, in addition to ensuring that errors are programmatically associated with specific form inputs, visual indicators for errors are also necessary. When providing visual indication, be sure that sighted users know what the error is and know how to fix the error.