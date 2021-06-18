# Meaningful Group Labels

## Group labels MUST be meaningful.

To assist users in successfully completing a form, provide labels that are clear and informative. Users should know up front exactly what is needed in order to submit the form successfully.

### Example

The fields below are separated into four `<fieldset>` elements with `<legend>` elements that provide both the step number and the information being gathered.

```html
<fieldset>
    <legend>Step 1: Pick Your Car</legend>
    <input type="radio" id="porsche9996" name="car"> <label for="porsche9996">Porsche 911</label>
    <input type="radio" id="mustang9996" name="car"> <label for="mustang9996">Ford Mustang</label>
    <input type="radio" id="nissan9996" name="car"> <label for="nissan9996">Nissan 370Z</label>
</fieldset>

<fieldset>
    <legend>Step 2: Pick Your Exterior Color</legend>
    <input type="radio" id="red9996" name="ecolor"> <label for="red9996">Red</label>
    <input type="radio" id="silver9996" name="ecolor"> <label for="silver9996">Silver</label>
    <input type="radio" id="black9996" name="ecolor"> <label for="black9996">Black</label>
</fieldset>

<fieldset>
    <legend>Step 3: Pick Your Interior Color</legend>
    <input type="radio" id="gray9996" name="icolor"> <label for="gray9996">Light Gray</label>
    <input type="radio" id="camel9996" name="icolor"> <label for="camel9996">Camel</label>
    <input type="radio" id="char9996" name="icolor"> <label for="char9996">Charcoal</label>
</fieldset>

<fieldset>
    <legend>Step 4: Pick Your Delivery Timeframe</legend>
    <input type="radio" id="short9996" name="delivery"> <label for="short9996">2-4 weeks</label>
    <input type="radio" id="medium9996" name="delivery"> <label for="medium9996">1-2 months</label>
    <input type="radio" id="long9996" name="delivery"> <label for="long9996">3-6 months</label>
</fieldset>
```

## Group labels MUST NOT rely solely on references to sensory characteristics.

Relying on sensory characteristics — such as references to shape, size, visual location, orientation, or sound — to provide labels for form controls has the potential to exclude users from understanding the labels. 

For instance, assuming everyone can see the shape, color, or iconography of a control may exclude users who are blind, colorblind, and some users who have low vision. Some things to keep in mind:

If color is used in a form control label, ensure that there is a non-color distinguishing factor such as text or an easily-recognizable symbol or icon.

The color contrast of text and symbols or icons used as label must meet minimum color contrast ratio requirements.
All information conveyed visually by a form label must be provided programmatically for assistive technology users.

### Example

```html
<fieldset>
  <legend>To make your meal, choose one appetizer, one main course, and one dessert from the options below.</legend>
  <fieldset>
    <legend>Appetizers</legend>
    <input type="checkbox" name="meal" value="shrimp" id="shrimp1"> <label for="shrimp1" style="color: green">Shrimp cocktail</label><br>
    <input type="checkbox" name="meal" value="potato" id="potato1"> <label for="potato1" style="color: green">Loaded potato skins</label><br>
    <input type="checkbox" name="meal" value="pizza"  id="pizza1"> <label for="pizza1" style="color: green">Flat bread pizza</label>
  </fieldset>
  <fieldset>
    <legend>Main Courses</legend>
    <input type="checkbox" name="meal" value="wings" id="wings1"> <label for="wings1" style="color: red">Buffalo chicken wings</label><br>
    <input type="checkbox" name="meal" value="tuna" id="tuna1"> <label for="tuna1" style="color: red">Seared tuna with mixed greens</label><br>
    <input type="checkbox" name="meal" value="pasta" id="pasta1"> <label for="pasta1" style="color: red">Pasta primevera</label>
  </fieldset>
  <fieldset>
    <legend>Desserts</legend>
    <input type="checkbox" name="meal" value="cheese" id="cheese1"> <label for="cheese1" style="color: blue">Cheese plate</label><br>
    <input type="checkbox" name="meal" value="torte" id="torte1"> <label for="torte1" style="color: blue">Chocolate torte</label><br>
    <input type="checkbox" name="meal" value="fruit" id="fruit1"> <label for="fruit1" style="color: blue">Fresh fruit and ice cream</label>
  </fieldset>
</fieldset>
```
