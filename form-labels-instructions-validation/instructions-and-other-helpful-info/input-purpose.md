# Input Purpose

## The purpose for each common input field that collects an individual's personal data MUST be programmatically defined based on the list of 53 Input Purposes for User Interface Components.

The intent of this success criterion is to programmatically provide additional information about form inputs (like address, phone number, and password fields) so that the information can be outputted to different modalities. Assistive technologies can use this information to help the user in various ways, including automatically completing forms, filling in usernames and passwords, and pairing custom icons with form elements for users who prefer using images for communication.

The W3C provides a [full list of inputs covered by this criterion](https://www.w3.org/TR/WCAG21/#input-purposes) which is built on the input purposes included in HTML 5.2 Autofill, so using HTML 5.2 Autofill is a good way to meet this success criterion.

This success criterion only applies to text inputs asking for information about the user themselves. It does not apply to text inputs asking for information about anyone other than the user, and it does not apply to any input types that are not text.

Success Criterion 1.3.6 “Identify Purpose” is level AAA and builds on this requirement.

### Example

The image below shows the login screen for Deque University, which is created using the HTML autocomplete attribute. When a user starts to input their email and password, they can quickly auto fill them if they’ve previously saved them.

```html
<input class="loginPassword" type="password" id="loginPassword" name="password" aria-required="true" autocomplete="current-password" required="required" oninvalid="this.setCustomValidity('Enter password to login')" oninput="this.setCustomValidity('')"/>
```