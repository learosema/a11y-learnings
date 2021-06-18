# One Label for multiple fields

## When one label is used for multiple elements, the label MUST be programmatically associated with each of the corresponding elements.

Some forms are designed with data fields split into multiple parts, such as a phone number, social security number, or an extended zip code. 

There are three main techniques for supplying labels under these circumstances:

1.Combine the fields together to avoid having to label each one separately.
2. Use off-screen text with CSS to provide hidden labels. This technique uses the traditional `<label>` tag and is very robust, but perhaps less elegant than the aria-label technique.
3. Use aria-label to provide hidden labels. If you do this, you should probably also provide a traditional `<label>` for the first field, to allow users to click on the text to put the focus in the form field.
4. Use a `<fieldset>` for the visible label and hidden text for the other labels.

### Good example 

This example shows how individual fields can be labelled using off-screen text styled with CSS to be visually hidden.

```html
<label for="ssn1b">Social Security Number <span class="offscreen">first three digits</span>:
</label>
<input type="text" size="3" maxlength="3" id="ssn1b"> -
<label for="ssn2b" class="offscreen">Second two digits:</label>
<input type="text" size="2" maxlength="2" id="ssn2b"> -
<label for="ssn3b" class="offscreen">Last four digits:</label>
<input type="text" size="4" maxlength="4" id="ssn3b">
```

A couple of notes about this method:

- This method is more backward-compatible than the method of using aria-label, so if you're trying to support older browsers and older screen readers, this is the best method.
- It also has the advantage that none of the screen readers will repeat any of the labels, so it sounds perfect in all screen readers.
