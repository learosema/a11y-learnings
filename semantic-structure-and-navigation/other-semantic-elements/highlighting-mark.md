# Highlighting (`<mark>`)

## Highlighted text SHOULD be marked with the `<mark>` element.

Sighted users will benefit from seeing important passages highlighted, if it is appropriate for the context of the text. The semantically-correct element to use is the `<mark>` element. The default styling in browsers is to highlight the text with a yellow background color. The visual styling can be customized via css.

Good Example: The `<mark>` element is used to highlight important text

```html
<p>All informative images <mark>require</mark> valid, meaningful alternative text.</p>
```

## Screen Readers and mark Element

Even though the `<mark>` element is semantically-correct, current screen readers do not notify users that a `<mark>` element is present, so there is no benefit to screen reader users (even though sighted users still benefit, because of the visual background color highlighting). That said, the `<mark>` element is still the best choice because that tag conveys the intended purpose (to mark something as highlighted).

## Critical highlighted text SHOULD be supplemented with a text-based method to convey the meaning of the highlighting.
Most of the time, highlighting can be considered a visual enhancement that screen reader users do not need to be aware of. That said, if the meaning of the text is lost without the visual highlighting, you will need to supplement the highlighting with some text that screen readers can access, because screen readers do not notify users about CSS highlighting or the `<mark>` element.

The `<mark>` element ought to be sufficient, since it is a semantic element, but you will have to employ workarounds if readers need to know about the highlighting. One way is to insert text that is visually hidden at the beginning and at the end of each highlighted section.

### Example

Only use if the meaning would be lost if the highlighting were not pointed out to users.

```html
<p>The woman <mark>
  <span class="visually-hidden">begin highlight</span>
    threw
  <span class="visually-hidden">end highlight</span>
  </mark> the Frisbee.
</p>
```