# Instructions for forms, groups and sections

## Instructions for groups or sections SHOULD be programmatically associated with the group.

Putting regular text in the middle of a form runs the risk that screen reader users will not hear it because if they're tabbing only to focusable elements, they will skip over all non-focusable text, unless that text is programmatically associated with a group label or an input.

Although there is a natural way to create a group label with `<fieldset>` and `<legend>`, there is no natural way to create a description that is associated with a group. Adding aria-describedby to either the `<fieldset>` or `<legend>` element doesn't work, so we have to get a bit more creative.

### Option 1: legend

Add the instructions to the `<legend>`. If the instructions are short, adding them to the `<legend>` is easy and unobtrusive. Some screen readers read the full `<legend>` text on every form field, though, so if the instructions are long, it can be annoying to hear them repeated over and over. In some ways, this is not semantically ideal, because the instructions are not the name of the group, but this method works, so it can be an acceptable workaround.
### Option 2 : aria-describedby

Associate the instructions with one of the fields (usually the first field is best) within the group, using aria-describedby. This way, the group instructions will be read only once, and they will not be skipped over by screen reader users if they're tabbing to focusable elements.

### Option 3: instructions associated with multiple form fields

Put the instructions before the start of the whole form, as regular text not associated with anything, and hope that screen reader users read them before jumping in to form mode. This option sidesteps the whole problem and puts the burden on the user, which is not ideal. 

Still, you could make a case that the text is available to them this way, as long as they read through the document sequentially, which many users are likely to do anyway. Just don't put the text in the middle of the form unless you associate it with one of the inputs. Screen reader users are much more likely to skip over disassociated text.

### Example 1: legend

```html
<fieldset>
<legend>Login Information (Required)</legend>
  <label for="username">Username: </label> 
  <input type="text" id="username"></p>
  <label for="password">Password: </label> 
  <input type="password" id="password"></p>
</fieldset>
```

### Example 2: aria-describedby

```html
<fieldset>
<legend>Create Account</legend>
  <p><label for="username">Username: </label> 
    <input type="text" id="username"></p>
  <p id="mustmatch">Password fields must match</p>
  <p><label for="password">Password: </label> 
    <input type="password" id="password" aria-describedby="mustmatch"></p>
  <p><label for="password2">Re-enter password: </label> 
    <input type="password" id="password2"></p>
</fieldset>
```

### Example 3: instructions associated with multiple form fields

```html
<fieldset>
<legend>Create Account</legend>
  <p><strong>Username and password
  <span id="mustnot">must not contain spaces</span></strong></p>
  <p><label for="username">Username:</label> 
    <input type="text" id="username" aria-describedby="mustnot"></p>
  <p><label for="password">Password:</label> 
    <input type="password" id="password" aria-describedby="mustnot"></p>
</fieldset>
```

## Instructions for groups or sections MUST be programmatically determinable.

When instructions are provided for forms and sections of forms, it is important that real text or text that is available through an alternative method is used. Assistive technologies like screen readers need to be able to access actual text in order to render information to assistive technology users.

If programmatically determinable text is not provided either through real text or through attributes like aria-label, aria-labelledby, aria-describedby, or even the alt if images are used, it would be nearly impossible for assistive technologies to access the text.

## Instructions for groups or sections MUST be meaningful.

To assist users in successfully completing a form, instructions must be clear, accurate, and informative. Users should know up front what is exactly needed in order to submit the form successfully, especially if there are specific expectations regarding the information users provide in a form.

## Instructions for groups or sections MUST be visible.

For sighted users and users who have low vision, form instructions for groups and sections must be clearly visible. Presenting instructions only through aria-describedby would only be available to screen readers users; and instructions that are presented through small text may be difficult for anyone to see, especially for people who have low vision.

## Instructions for groups or sections SHOULD be visually adjacent to the grouped elements.

For people who use screen magnification, if instructions are too far away from the form groups and sections, they may miss the information or need to constantly scroll back and forth to make the connection between the form fields and their instructions. Placing the instructions close to the form group will make it easier for these users to navigate through the form itself.

## Instructions for groups or sections SHOULD be adjacent in the DOM to the grouped elements.

Screen readers generally read and interpret content the way it is presented in the DOM. So, ensuring that instructions are placed near the elements they describe in the DOM might prevent confusion for screen reader users as they navigate through forms.

For instance, if there are instructions provided for the entire form, then those instructions should come just before the form itself in the DOM. The same applies to groups or sections within a form.

In most cases, if the instructions are visually adjacent to the elements they're describing, the instructions will also be adjacent in the DOM, but if CSS is used for visual placement, it's possible to have the instructions separated from their elements in the DOM even if they visually look adjacent.

## If the instructions are not critical to understand the purpose of a group or section, the instructions MAY be hidden until the user requests them.

If there are instructions that may help a user complete a section in a form but aren't critical to the user successfully completing the form fields, instructions can be hidden until the user requests to read those instructions.

## Instructions for groups or sections MUST NOT rely solely on references to sensory characteristics.

Relying on sensory characteristics to provide instructions for form groups and sections has the potential to exclude users from receiving those instructions. For instance, relying on color alone to convey instructions excludes users who are blind, colorblind, and some users who have low vision. 

However, relying only on programmatic association like `aria-labelledby` or `aria-describedby` excludes users who are sighted or may not use a screen reader. Instructions should be accessible to both assistive technology users and users who don't use assistive technology.

### Bad

- use color indicators like red/green to convey which fields are required/optional

