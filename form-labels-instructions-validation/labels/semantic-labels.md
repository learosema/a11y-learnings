# Semantic Labels

## Labels MUST be programmatically associated with their corresponding elements.

Every form input and control needs a label, also known as an "accessible name." The label must be programmatically associated with the input, to remove all ambiguity. There are multiple ways of providing labels. Under most circumstances, the best way is to use the HTML `<label>` element, because that's what it was designed to do.

It has the broadest support and has the added benefit that mouse users can click on either the input OR the label to put the focus in the input, thus increasing the click target size. 

A larger click target size is helpful for users with tremors or other difficulties in fine motor control, and for mobile users, especially when the click target is very small, like a single radio button.

There is a hierarchy of methods for providing an accessible name for an input:

- aria-labelledby
  - visible as text and accessible to screenreaders
  - but clicking does not put the focus in the associated form input
- aria-label
  - invisible, only accessible to screenreaders, so mostly a bad choice
- `<label>` - recommended method for most circumstances
- title attribute
  - usually intended for extra, non-essential information
  - mostly invisible, adds a tooltip on hover, which can be useful to mouse users (but not keyboard users)
  - so generally not recommended 
- placeholder
  - technically allowed as a way to privide an accessible name, but highly discouraged
  - disappears when users start typing
  - default styling fails contrast rules
  - intended use is for extra, non-essential information

Screen readers depend on accurate labels to convey the purpose of the form input to users. If an input does not have a programmatically-associated label, but it does have adjacent text, some screen readers (JAWS and VoiceOver in particular) will make an educated guess that the adjacent text is supposed to be the label, even if it isn't marked as such. 

In most instances the screen readers guess correctly, but sometimes they don't.

## Example: explicit label

```html
<p>
  <label for="fname_a">First Name:</label> 
  <input type="text" name="fname_a" id="fname_a">
</p>
<p>
  <label for="lname_a">Last Name:</label>
  <input type="text" name="lname_a" id="lname_a">
</p>
```


## Example: implicit label

An implicit association is created by putting the form control inside the label element.

```html
<p>
  <label>First Name: <input type="text" name="fname1"></label>
</p>
<p>
  <label>Last Name: <input type="text" name="lname1"></label>
</p>
```

### Note

There have been some edge cases in which some browsers and/or screen readers lacked support for implicit labels in very specific circumstances, such as the `<input type="number">` element in Firefox with the NVDA screen reader opens in a new window, but overall support is solid for this method.

## Labels MUST be available as programmatically determinable text.

It is not enough to just have a label. The label must contain programmatically determinable text that assistive technologies can read. 

An empty label is just as bad as having no label at all. In fact, it can be worse, because the screen readers that try to guess at the label when no label is specified will not guess at all if a label is properly specified. 

And if the properly specified label has no text to read, the assistive technology will have nothing to convey to the user.

