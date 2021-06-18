# Multiple Labels for One Field

## When multiple labels are used for one element, each label MUST be programmatically associated with the corresponding element.

Sometimes it is necessary to associate more than one label to a form field. The problem is that a `<label>` and a form element must have a one-to-one relationship: the `<label>` element can only be associated with one form element and a form element can only be associated with one `<label>` . In this case, aria-labelledby is a useful tool to associate multiple labels with a single field.

A classic example of when you might want to associate multiple labels with a field is when a form is formatted inside of a table, and the form fields are labeled by the table's row and column header cells. Unfortunately, screen readers cannot automatically apply table headers to form elements, so you must use another method. This is where aria-labelledby becomes very useful.

### Good example: assigning multiple labels to one form element

In the table below, each form element needs to be labeled by more than one table header, and each table header must provide labels for more than one form element.

For example, the first checkbox corresponds to "Now" and "Food stamps." Screen reader users need to hear both of those labels when they tab to that checkbox. The "Now" header also applies to the other two checkboxes in the same column, and the "Food stamps" header applies to the other two form elements in that row.

The first step in making a table-based form accessible is to make the table itself accessible by applying the appropriate row and/or column headers. Once the appropriate table markup is in place, you can use aria-labelledby to use the table headers as the labels for the form elements.

To associate multiple headers with a form element, type the id of each header, separated by a space. For example, to associate a form element with two items with id="now" and id="foodstamps" you would type: 

```html
aria-labelledby="now foodstamps"
```

In more complex tables, it is possible to have three or more labels associated with a form element (each separated by a space in the aria-labelledby attribute), but such complexity is probably not a good idea, in terms of overall usability.

```html
<table>
<caption>Edit Program Information</caption>
  <tr>
    <th scope="col"><span id="program">Program</span></th>
    <th scope="col"><span id="now">Now</span></th>
    <th scope="col"><span id="past">Past</span></th>
    <th scope="col"><span id="date">Date</span></th>
  </tr>
  <tr>
    <th scope="row"><span id="foodstamps">Food stamps</span></th>
    <td><input type="checkbox" name="checkbox"
      aria-labelledby="now foodstamps"></td>
    <td><input type="checkbox" name="checkbox2"
      aria-labelledby="past foodstamps"></td>
    <td><input type="text" name="textfield"
      aria-labelledby="date foodstamps"></td>
  </tr>
  <tr>
    <th scope="row"><span id="tca">TCA</span></th>
    <td><input type="checkbox" name="checkbox3"
      aria-labelledby="now tca"></td>
    <td><input type="checkbox" name="checkbox4"
      aria-labelledby="past tca"></td>
    <td><input type="text" name="textfield2"
      aria-labelledby="date tca"></td>
  </tr>
  <tr>
    <th scope="row"><span id="medical">Medical</span></th>
    <td><input type="checkbox" name="checkbox5"
      aria-labelledby="now medical"></td>
    <td><input type="checkbox" name="checkbox6"
      aria-labelledby="past medical"></td>
    <td><input type="text" name="textfield3"
      aria-labelledby="date medical"></td>
  </tr>
</table>
```

#### Important note

Note that the table headers/labels are in <span> tags and that it is the <span> tag and NOT the <th> tag that has the id. If you place the id on the <th>, some screen readers will not read the labels correctly when you tab through the form elements.