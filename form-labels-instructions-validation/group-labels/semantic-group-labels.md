# Semantic Group Labels

## Group labels MUST be programmatically associated with the group if the individual labels for each element in the group are insufficient on their own.

When a group of related form fields shares a group label, the group and corresponding label must be expressed semantically, so that people using a screen reader can understand the relationship of the form fields, their individual labels, and their group label.

Grouping controls is most important for related radio buttons and checkboxes. Associating a label with an individual radio button or checkbox is required, but alone is not enough. Knowing a radio button has a label of "yes" or "no" is not useful if the user does not know what question they are answering. While a person who can see the screen can see the relationship between a group label and the radio buttons to which it applies, a screen reader user may not understand that relationship if it is not expressed semantically. The same concept can be applied to other groups of form fields such as a grouping of mailing address and billing address fields.

Related form controls can be programmatically grouped using HTML or ARIA techniques:

The HTML solution consists of using a `<fieldset>` to semantically group the form fields and a `<legend>` to provide a semantic group label.
The ARIA solution consists of semantically grouping fields within a group region and providing a semantic group label using the aria-labelledby attribute.

### Example with fieldset

The `<fieldset>` tag groups form elements visually by placing a box around them. It also groups them programmatically by applying the `<legend>` as the label for the group, so that screen readers can read the label when users arrive at the group.

Some screen readers, like JAWS and VoiceOver, read the `<legend>` text with every field inside the `<fieldset>`. Most screen readers read the `<legend>` first. VoiceOver reads the label of the form field first, then the `<legend>`, which sound backwards, but that's out of the developer's control, and regular VoiceOver users will be used to hearing things that way.

```html
<form>
  <fieldset>
    <legend>Contact Information</legend>
    <p><label for="name6044">Name: </label> <input type="text" id="name6044"></p>
    <p><label for="phone6044">Phone: </label> <input type="text" id="phone6044"></p>
    <p><label for="email6044">Email: </label> <input type="text" id="email6044"></p>
    <p><label for="address6044">Address: </label> <input type="text" id="address6044"></p>
    <p><label for="city6044">City: </label> <input type="text" id="city6044"></p>
    <p><label for="state6044">State: </label> <input type="text" id="state6044"></p>
    <p><label for="zip6044">Zip: </label> <input type="text" id="zip6044"></p>
  </fieldset>
</form>
```

### Example with aria

ARIA can also be used to group a set of related form fields and programmatically associate a group label with them. The related form fields are placed within a container, such as a `<div>`. The container is given the ARIA role of group and an aria-labelledby attribute that references an id on the group label. Using this ARIA technique will not place an outline around the grouped fields.

Note: VoiceOver does not yet support role="group" as a way to label a group of form elements. For this reason, `<fieldset>` and `<legend>` are still preferred over role="group".

```html
<p id="grouplabel9961">Contact Information</p>
<div role="group" aria-labelledby="grouplabel9961">
    <p><label for="name">Name: </label> <input type="text" id="name"></p>
    <p><label for="phone">Phone: </label> <input type="text" id="phone"></p>
    <p><label for="email">Email: </label> <input type="text" id="email"></p>
    <p><label for="address">Address: </label> <input type="text" id="address"></p>
    <p><label for="city">City: </label> <input type="text" id="city"></p>
    <p><label for="state">State: </label> <input type="text" id="state"></p>
    <p><label for="zip">Zip: </label> <input type="text" id="zip"></p>
</div>
```

### Example: nested fieldsets

Nested `<fieldset>` elements are permitted to create groups inside of groups.

Note: Some older versions of some screen readers used to read both the outer `<legend>` and the inner `<legend>` on every field when inside nested `<fieldset>` elements, making the experience highly redundant. Modern screen readers have improved the user experience. They read only the inner `<legend>` text when on a field inside a nested field`<fieldset>`set.

```html
<fieldset>
  <legend>Contact Information</legend>
  <p><label for="name6045">Name: </label><input type="text" id="name6045"></p>
  <p><label for="phone6045">Phone: </label><input type="text" id="phone6045"></p>
  <p><label for="email6045">Email: </label><input type="text" id="email6045"></p>
  <p><label for="address6045">Address: </label><input type="text" id="address6045"></p>
  <p><label for="city6045">City: </label><input type="text" id="city6045"></p>
  <p><label for="state6045">State: </label><input type="text" id="state6045"></p>
  <p><label for="zip6045">Zip: </label><input type="text" id="zip6045"></p>
  <div class="mode-radio">
      <fieldset>
          <legend>Preferred mode of communication:</legend>
          <p><input type="radio" name="mode" id="mode-phone6045"> 
            <label for="mode-phone6045">Phone</label><br>
          <input type="radio" name="mode" id="mode-email6045"> 
            <label for="mode-email6045">Email</label></p>
      </fieldset>
  </div>
</fieldset>
```


## Group labels MUST be programmatically determinable.

Neither the HTML specifications nor WCAG require that every `<fieldset>` have a `<legend>`. However, in practice, if a `<fieldset>` is used to group labels, a group label is usually required to describe the grouping. For example, radio buttons and grouped check boxes (almost) always require a group label to describe their purpose.

When a group label is required to adequately describe the group of fields, it must be programmatically associated with the grouping using a `<legend>` (or aria-labelledby if using the ARIA technique).