# Table caption/name

## Data tables SHOULD have a programmatically-associated caption or name.

Screen readers read the caption or name of the table when users navigate to the table, giving users a sense of what the table is about. The `caption` element is the most straightforward way to give a name to a table. It is also possible to use aria-label or aria-labelledby.

Note that the text in the aria-label attribute is invisible to sighted users.

### Examples
#### Using `caption`

```html
<table>
  <caption>1st Quarter Results</caption>
```

#### Using `aria-label`

```html
<table aria-label="1st Quarter Results">
```

#### Using `aria-labelledby`

```html
<h3 id="tableCaption">1st Quarter Results</h3>
<table aria-labelledby="tableCaption">
```

#### Using `figcaption` with `aria-labelledby`

```html
<figure>
<table aria-labelledby="figCaption">
<!-- the rest of the table goes here -->
</table>
<figcaption id="figCaption">Fourth Quarter Results</figcaption>
</figure>
```

## The name/caption of a data table SHOULD describe the identity or purpose of the table accurately, meaningfully, and succinctly.

The purpose of the caption or name is to allow users to identify the table and/or understand the purpose of the table, so the caption or name should be meaningful. Just saying "Table 1," for example, would not be helpful. An alternative would be "Table 1: First Quarter Earnings."

## The name/caption of each data table SHOULD be unique within the context of other tables on the same page.

If there are two or more tables on the same page with the same caption or name, screen reader users will not be able to distinguish the tables when they pull up the list of all of the tables on the page.
