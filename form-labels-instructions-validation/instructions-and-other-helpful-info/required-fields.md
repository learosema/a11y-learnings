# Required Fields

## Overview

Clearly identifying required fields helps prevent user errors and it reduces the chance that users will neglect to fill out all necessary fields in a form. The general requirements for identifying required fields are:

- The aria-required="true" indicator should be set on the input.
- A supplemental visible indicator should be available to sighted users.

##  Required fields SHOULD be programmatically designated as such.

### `aria-required="true"`

Setting aria-required="true" on an input is an unambiguous way to designate the field as required. Screen readers say "required" after reading the input's label. This attribute is invisible, though, so you will need to supplement it with some other method that sighted users can see.

#### Example with aria-required

```html
<p>Fields with asterisks (*) are required.</p>
<p>
<label for="firstname">First Name:*</label> 
<input id="firstname" name="firstname" type="text" aria-required="true">
</p>
<p>
<label for="lastname">Last Name:*</label> 
<input id="lastname" name="lastname" type="text" aria-required="true">
</p>
<p>
<label for="age">Age:</label> 
<input id="age" name="age" type="text">
</p>
```

### HTML 5 required

The HTML 5 required attribute sounds the same to screen reader users — they hear "required" after the input's label — but the HTML 5 attribute adds a browser behavior (in browsers that support it): it prevents users from submitting the form if there are errors.

That can be a good thing in theory, but not all browsers support it, and this takes away some of your freedom to design the error handling behavior, so use this one very cautiously. Also: it's invisible; sighted users can't see it.

## Required fields SHOULD have a visual indicator that the field is required.

Again, it is best to try to prevent users from making mistakes while completing a form. In addition to identifying required fields programmatically, required fields should be identified to sighted users so they are aware also as to what fields need to be completed.

### Example

"Fields with asterisks (*) are required."

```html
<p>Fields with asterisks (*) are required.</p>
<p>
<label for="firstname">First Name: *</label>
<input id="firstname" name="firstname" type="text" aria-required="true">
</p>
<p>
<label for="lastname">Last Name: *</label>
<input id="lastname" name="lastname" type="text" aria-required="true">
</p>
<p>
<label for="age">Age:</label> 
<input id="age" name="age" type="text">
</p>
```

## The form validation process MUST include an error message explaining that a field is required if the field isn't identified as required both visually and programmatically in the form's initial state.

If the form's initial state does not identify required fields programmatically and visually, then this information must be conveyed after the users attempt to submit a form, through an error message.

It is critical that error messages are associated programmatically to the corresponding required fields so that assistive technology users do not have to hunt for the errors within the form. It would also be best practice to provide a visual indication of errors for sighted users so that they can quickly identify the fields with errors.

### Example: Identifying errors visually and programmatically

In the input fields below, the error message is programmatically associated through aria-describedby. A sighted user can see the message and a screen reader user can hear that the date is required.

```html
<p>
  <label for="username">Username:</label>
  <input type="text" name="username"
    id="username" value="User name">
</p>
<p class="error">
  <label for="expire">Expiration:</label>
  <input type="text" name="expire" id="expire"
    aria-required="true"
    aria-invalid="true"
    aria-describedby="expDesc">
  <span id="expDesc">Error: Date is required.</span>
</p>
``` 

### Example: Error summary

For this example, a summary is provided that tells users how many errors are in the form, then explains what kind of errors they are. In addition to providing a link to the first error, aria-required and aria-invalid are used to communicate to users programmatically that the fields are required and that their entries are invalid.

```html
<div class="alert">
<p><strong>Error:</strong>
  There are 2 fields with problems in this form:</p>
  <ol>
      <li><strong>First Name</strong> cannot be blank</li>
      <li><strong>Last Name</strong> cannot be blank</li>
  </ol>
<a href="#fname" id="errorSummaryLink">Go to the first field with an error to fix it</a>.
</div>

<label for="fname">First Name:</label><br>
<input type="text" id="fname" aria-required="true" aria-invalid="true">
<label for="lname">Last Name:</label><br>
<input type="text" id="lname" aria-required="true" aria-invalid="true">
```