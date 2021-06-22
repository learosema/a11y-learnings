# Name

## The "accessible name" calculation algorithm

The accessible name of an element is calculated using a rather complicated algorithm. A simplified version of this algorithm is shown below:

### `aria-labelledby`

If there is an `aria-labelledby` attribute, the text it refers to will override all other name and label methods.

### `aria-label`

If there is no `aria-labelledby`, the `aria-label` text string will override everything else. Note that the `aria-label` text is invisible, and only available to assistive technology users.

### The native HTML text of the element (or native label or alternative text)

If there is no `aria-labelledby` or `aria-label`, the native text of an element will be used (e.g. the text between the opening and closing `<button>` elements, the `<label>` text on a form field, the alt text of an image, etc.

### title
If no other naming methods are available, the title will count as the label. Note that the title is best considered as extra, non-essential information, because the title is not visible at all times and some users cannot access it at all, for example in browsers that show the title text only on mouse hover.

### Important:
Always plan to use the native HTML methods of labeling first. Only use `aria-labelledby` or `aria-label` if no other method works well in the context at hand.

## `aria-labelledby`

### The `aria-labelledby` Text Is (Usually) Visible on the Page

In nearly every case, the `aria-labelledby` text is already visible on the page. The point in using `aria-labelledby` is to link the element with its label so that screen readers can associate the two programmatically in the way that sighted users associate the two visually.

In some rare cases, you may refer to text that is visually hidden, and that may be appropriate for some things, but you may be putting sighted users at a disadvantage when you do that, so think carefully before you hide a label.

### The `aria-labelledby` Attribute Refers to the id of Another Element

You type the id of another element with `aria-labelledby`. You don't type the label text itself.

```html
<div class="modal" role="dialog" tabindex="0" aria-labelledby="h1">
<h1 id="h1">Confirm your selection</h1>
```

### You Can Refer to Multiple IDs with `aria-labelledby`

One of the strengths of the `aria-labelledby` attribute is that it allows you to refer to multiple selections of text and apply them all together to label an element. This can be especially useful for labeling complex forms, such as those laid out in a grid in which multiple labels can apply to a single form field.

```html
<span id="males"> ... <span id="frank"> ... <span id="ranking"> 
<input type="text" aria-labelledby="males frank ranking">
```

### The `aria-labelledby` Text Replaces an Element's Original Text

Like `aria-label`, the text referenced by `aria-labelledby` is supposed to replace the original text of the element. Don't use `aria-labelledby` to provide supplemental information in addition to the text that's already there, because that's not what it will do in most circumstances. The `aria-describedby` attribute would be more appropriate for that purpose.

As with `aria-label`, screen reader behavior is not entirely consistent, so in some cases the screen reader will read both the original text and the `aria-labelledby` text, but don't count on that happening.

## `aria-label`

### The aria-label Contains the Label Text Itself

You write the label text as a part of the aria-label attribute itself.

```html
<nav aria-label="Clothing for Girls">
```

### The `aria-label` Text Is Invisible

The `aria-label` attribute creates an invisible label for an element that is available only to assistive technologies. 

Sighted users can't see it, and there is no visual indication that the label is present, so sighted users do not benefit from `aria-label` at all. There isn't even a pop-up tooltip. It really is completely invisible. Only assistive technology users benefit from it.

### The aria-label Text _Replaces_ an Element's Original Text

If you have a link and add aria-label to the link, whatever text you put in the aria-label will replace the original link text:

```html
<a href="http://w3.org" aria-label="The World Wide Web Consortium">W3C</a>
<!-- will not say W3C at all -->
```

With this in mind, be careful not to use `aria-label` to provide extra information about an element, because `aria-label` doesn't work that way. The `aria-label` text is not extra information. It is the ONLY information.

Admittedly, not all screen readers behave this way in all circumstances, so there are some situations in which the screen reader will say both the original text and the `aria-label` text, but you can't count on this. You should assume that `aria-label` will replace the original text, because that's what it is supposed to do, according to the official specification.

#### Example: using aria-label on landmark regions

```html
<nav aria-label="Product Categories">
<!-- an aria-label is needed when there are more than 1 nav on the site -->
```

#### Example: using aria-label on a site search

It is always best to provide a visual label for every form element. That being said, there are special cases where the visual proximity of other elements (like a "Search" button) could provide enough of a visual label for sighted users, and that a separate, explicit, text label may be unnecessary. 

```html
<form action="#" role="search">
  <input aria-label="Site Search" name="search" type="search">
  <input type="submit" value="Search">
</form>
```

As easy as it may be for sighted users to make sense of the above site search feature, blind users will have a harder time unless you provide an explicit label somehow. This is where the `aria-label` on the input comes in.

## Support for `aria-labelledby` and `aria-label`

The `aria-label` and `aria-labelledby` attributes allow you to assign a name or label to almost any HTML element: links, form fields, paragraphs, etc., though screen reader support is best on focusable elements, or on elements in application regions as explained later. 

In practice, screen reader support for `aria-label` and `aria-labelledby` is best on:

- Focusable elements (`<a>`, `<input>`, etc.). Support is not as good on non-focusable elements (`<p>`, `<div>`, `<span>`, `<h1>`, etc.).
- Elements with semantic meaning, as opposed to the elements that do not have semantic meaning (like `<div>` and `<span>`).
- Application regions (role="application"). But be very careful with application regions, because they disable most of the screen reader's regular keyboard shortcuts.

In principle, you ought to be able to apply `aria-label` to any HTML element, whether it is a paragraph, heading, form element, link, image, or anything else. 

In practice, the `aria-label` attribute is supported better on some elements than on others, and not all screen readers — or versions of the same screen reader — support `aria-label` in the same way. 

To complicate matters, the support for `aria-label` is generally better when labeling an item inside an application region (a section of the web page marked as role="application") than when labeling an item in a regular document area of the web page. 

Even more confusing, the support may depend on what screen reader mode you are using. For example, if you let the screen reader read straight through the document (in document or reading mode), it may not read the `aria-label` value on some elements, but when you navigate sequentially by element, or if you tab to the element (in form reading mode), the same screen reader may read the `aria-label` value.

And to add yet another layer of complexity, different browsers or versions of the same browser may behave differently with the same brand of screen reader.

A somewhat oversimplified summary is that support for `aria-label` is best:

- on focusable elements (`<a>`, `<input>`, etc.), or
- on elements inside an application region (e.g. `<div role="application">`)

