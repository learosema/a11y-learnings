# Instructions for inputs

## Overview

In order to make instructions for individual form inputs accessible, instructions must be composed using discernible text that is associated programmatically with the individual input.

Furthermore, instructions should be visible to users who can see and in close proximity to the input fields for users who have low vision.

Instructions must be specific and meaningful in a manner that users know what to do to complete the form fields; and instructions must not rely solely on sensory characteristics like sight or hearing as they may exclude users who have sensory disabilities.

## Instructions for an element MUST be programmatically associated with the element.

If there are specific instructions for entering information within a particular form input, or specific instructions for buttons or controls, the instructions must be programmatically associated with its corresponding input or control.

Though this technically can be done by providing instructions within the `<label>` element, when it comes to semantics, the most appropriate way to associate instructions is by using the `aria-describedby` attribute.

### Example

```html
<p>
  <label for="email">Email:</label>
  <input type="email" name="email" id="email" 
    aria-describedby="input-instructions">
  <span id="input-instructions">(Must be a valid email address)</span>
</p>
```

## Instructions for an element MUST be available as programmatically determinable text.

Text that assistive technologies can access must be provided for form inputs. Without programmatically determinable text, assistive technologies like screen readers cannot render information to users.

The easiest way to provide programmatically determinable text is to include the text in the `<label>`, but programmatically determinable text can also be provided through ARIA attributes like `aria-label` and `aria-labelledby`.

## Instructions for an element MUST be available as programmatically determinable text.

Text that assistive technologies can access must be provided for form inputs. Without programmatically determinable text, assistive technologies like screen readers cannot render information to users. 

The easiest way to provide programmatically determinable text is to include the text in the `<label>`, but programmatically determinable text can also be provided through ARIA attributes like aria-label and aria-labelledby.

### Example

```html
<p>
  <label for="upload">Upload file</label> 
  <span id="desc">in MS Word format</span> <span class="far fa-file-word fa-lg"></span>:
  <input type="file" id="upload" aria-describedby="desc">
</p>
```

## Instructions for an element MUST be meaningful.

If a form field requires a certain format or other specific instructions — letting the users know this ahead of time can help avert errors before they happen.

For instance, in the example below, providing the correct format for the date is critical to properly submitting the information requested. Not providing this necessary detail will increase the chances that the user will make a mistake.

### Example

'Enter valid date' is not specific enough, instead: 'Enter date as MM/YYYY'.

```html
<form>
  <label for="date">Date: </label>
  <input type="text" name="date" id="date" aria-describedby="dateinstructions">
  <span id="dateinstructions">Enter date as MM/YYYY.</span>
</form>
```

## Instructions for an element MUST be visible.

In addition to the requirement that instructions must be programmatically associated with their corresponding inputs, we cannot forget that instructions must also be visible for sighted users. 

This is important because instructions can be provided programmatically for assistive technology users using techniques such as ARIA or clipped text without necessarily being visible on the screen. To complete the form effectively, sighted users must not be excluded from instructions that are supplied for individual form elements.

## Instructions for an element SHOULD be visually adjacent to the element.

If the labels, instructions, or advisory information are too far away from their corresponding form fields, people using screen magnification may not see them, because screen magnification reduces the visible area of the screen.

## Instructions for an element SHOULD be adjacent in the DOM to the element.

As mentioned on the previous page, screen readers render information to users from the DOM. So, it makes sense that specific instructions for form fields be placed near the form fields themselves for screen reader users to easily detect that information.

### Example

```html
<form>
<p id="instructions"><strong>Create a password that is at least 8 characters long 
and includes both letters and numbers.</strong></p>
<label for="password">Password: </label>
  <input type="password" name="password" id="password" 
  aria-describedby="instructions">
</form>
```

## If the instructions for an element are not critical, the instructions MAY be hidden until the user requests them.

If you would like to provide users with helpful instructions for completing a form input, but the instructions aren't necessarily required to complete the input field, you can hide this information and allows users to access it if they want to access the information.

### Example

```html
<p>
  <label for="id88_password1">Password </label><button aria-label="Password instructions" id="password-instructions"><img src="images/reference/question-mark-icon-16.png" alt="Passwordinstructions"></button>
  <input type="password" name="id88_password1" id="id88_password1">
</p>
```

## Instructions for an element MUST NOT rely solely on references to sensory characteristics.

Relying on sensory characteristics like visual location, shape, and sound to provide instructions can exclude some users from accessing those instructions. For instance, using a different text color to convey that a field is required excludes users who are blind, colorblind, and some low vision users from accessing that information. So, when instructions are provided, they should be clear and not rely solely on sensory characteristics that may exclude other users.

- Bad: Fields marked with red labels are required