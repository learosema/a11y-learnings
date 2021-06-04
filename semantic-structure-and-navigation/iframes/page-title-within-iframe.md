# Page Title Within an Iframe

## The source page of an iframe MUST have a valid, meaningful `<title>`.

Even though the WCAG guidelines require the title attribute, JAWS reads the `<title>` element of the enclosed document instead, if available. Only if the enclosed document does not have a `<title>` element will JAWS read the title attribute of the `<iframe>`. 

This behavior of giving priority to the enclosed document's `<title>` is a bit of a departure from the guidelines, but since all web pages are supposed to have meaningful `<title>` tags anyway, it shouldn't matter too much that JAWS behaves differently than the other screen readers in this regard. 

A best practice would be to give the enclosed document a `<title>` that matches the title attribute of the parent `<iframe>`. This would ensure the same title is read across different screen readers.