# `<blockquote>` and `<q>`

## The `<blockquote>` element SHOULD be used to designate long (block level) quotations.

Most desktop screen readers announce the blockquote element, so you can safely use it with the expectation that blind users will know that the content inside a blockquote is a quotation.

## The `<blockquote>` element SHOULD NOT be used for visual styling alone.

The visual styling of `<blockquote>` is indented on the left. It may be tempting to use `<blockquote>` purely for the visual indentation effect, but that will convey the wrong information to screen reader users if the information inside is not a quotation.

## The `<q>` element (for inline quotations) SHOULD NOT be used as the only way to designate quotations.

Even though the `<q>` element was invented as a way to designate inline quotations in a semantically-appropriate way that could be used by screen readers, most screen readers ignore this element completely, so for now it is best to simply use quotation marks (" and ').

