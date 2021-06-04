# Strikethrough/Delete and Insert

## Strikethrough text SHOULD be marked with the `<del>` element.

The semantically-correct element to use to mark deleted text is the `<del>` element. Visually, the default style for inserted text is a strikethrough line across the middle of the text.

### Note:
Screen readers do not support the `<del>` element. They read the text, but do not notify users that the text has been deleted.

## Critical strikethrough text MUST be supplemented with a text-based method to convey the meaning of the strikethrough.

```html
<p>Price reduced! 
  <del>
  <span class="visually-hidden">Was</span>
    $100
  </del> 
  <ins>
  <span class="visually-hidden">now</span>
    $75!
  </ins>
</p>
```

## Text designated for insertion SHOULD be marked with the `<ins>` element.

The semantically-correct element to use to mark inserted text (usually in legal documents) is the `<ins>` element. Visually, the default style for inserted text is an underline beneath the text.

### Note:

Screen readers do not support the `<ins>` element. They read the text, but do not notify users that the text has been inserted.

## Critical text designated for insertion MUST be supplemented with a text-based method to convey the meaning of the insertion.

```html
<p>If you can't say something nice, don't say 
  <del>
  <span class="visually-hidden">begin deleted text</span>
    nothing
  <span class="visually-hidden">end deleted text</span>
  </del> 
  <ins>
  <span class="visually-hidden">begin inserted text</span>
    anything
  <span class="visually-hidden">end inserted text</span>
  </ins>
  at all.
</p>
```