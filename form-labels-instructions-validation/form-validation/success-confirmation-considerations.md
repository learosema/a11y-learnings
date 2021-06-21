# Success Confirmation Considerations

## Success confirmation feedback SHOULD be programmatically determinable.

Again, in order for assistive technologies like screen readers to interact with and render messages to users, messages need to be composed using programmatically determinable text: either real text or text available through alternatives such as alt, aria-label, aria-labelledby, and aria-describedby. Just like with error messages, success messages also need to be available to assistive technology users.

### Example

```html
<div class="success">
  <p><span class="fa fa-check fa-4x" aria-label="Success"></span></p>
  <p>Your form has been successfully submitted.</p>
</div>
```

## Success confirmation feedback SHOULD be meaningful.

Just like with error messages, success messages should be clear, accurate, and informative. It helps to let users know exactly what was successful about their submission (e.g., Was the form submitted successfully? Were their files deleted? Preferences saved?). Be explicit in success messages so users don't have to guess at what was done successfully.

- Good: Your preferences have been saved.
- Bad: ok

## Success confirmation feedback MUST be visible.

Users who are sighted need to be able to see if they have been successful after interacting with a form or form controls.

In addition to providing programmatically determinable text for success messages, provide a visual indicator for users who are sighted or users who are sighted but do not use assistive technologies that require interaction with programmatically determinable text to interact with web content.

### Bad example: don't hide aria-live regions

```html
<div id="aria-live" aria-live="assertive" class="visually-hidden">
  Your preferences have been saved.
</div>
```