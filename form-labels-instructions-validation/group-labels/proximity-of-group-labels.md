# Proximity of group labels

## Group labels SHOULD be visually adjacent to the grouped elements.

If group labels are too far away from their corresponding form fields, people using screen magnification may have trouble finding them or may have to scroll back and forth or up and down to make the connection between form fields and their group label.

### Example

Don't put the img tag inside the fieldset:

```html
<p><img src="assets/images/module-forms/fireworks.png" height="196" width="625" alt="A firework"></p>
<fieldset>
<legend>Choose your top three favorite holidays:</legend>
    <input type="checkbox" name="holiday" id="memorial9134" value="Memorial"> <label for="memorial9134">Memorial Day</label><br>
    <input type="checkbox" name="holiday" id="july9134" value="July"> <label for="july9134">4th of July</label><br>
    <input type="checkbox" name="holiday" id="labor9134" value="Labor"> <label for="labor9134">Labor Day</label><br>
    <input type="checkbox" name="holiday" id="halloween9134" value=""> <label for="halloween9134">Halloween</label><br>
    <input type="checkbox" name="holiday" id="thanks9134" value=""> <label for="thanks9134">Thanksgiving</label><br>
</fieldset>
```

## Group labels SHOULD be adjacent in the DOM to the grouped elements.

When screen readers are reading a page using browse mode, they read information in the order it appears in the DOM. If group labels and their associated form fields are not adjacent to each other in the DOM, screen reader users may have trouble associating the group label and form fields as they are browsing a page.
