# Meaningful Label Text

## Labels MUST be meaningful.

To assist users in successfully completing a form, provide labels that are clear, informative, accurate, and meaningful. Users should know up front exactly what is needed in order to submit the form successfully.

## Labels MUST NOT rely solely on references to sensory characteristics.

Relying on sensory characteristics to provide labels for form controls has the potential to exclude users from understanding the labels.

For instance, assuming everyone can see the shape, color, or iconography of a control may exclude users who are blind, colorblind, and some users who have low vision. Some things to keep in mind:

- If color is used in a form control label, ensure that there is a non-color distinguishing factor such as text or an easily-recognizable symbol or icon.
- The color contrast of text and symbols or icons used as label must meet minimum color contrast ratio requirements.
- All information conveyed visually by a form label must be provided programmatically for assistive technology users.

### Example

In the example below, a text field and its label are followed by a small blue button containing the letter "i". Visually, it is apparent that the button will provide additional information about the text field. The aria-label for the button, "What does 'hue' mean?" provides a descriptive label for screen reader users.

```html
<label for="hue2">Favorite hue:</label> <input type="text" id="hue2"> 
<button aria-label="What does 'hue' mean?" id="hueButtonGood">
    <span class="fa fa-info-circle"></span>
</button>
```

