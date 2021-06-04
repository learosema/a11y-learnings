# Semantic structure across iframes

## Screen readers allow cross-frame navigation of semantic elements.

Screen readers treat an `<iframe>` almost as if it is part of the same document that contains it. Users can access all of the content within an `<iframe>` using the same keystrokes that they would use to access the content if it were all in the same document. For example, if there are 5 headings in the parent document and 3 headings in an iframe, the screen reader will list all 8 headings, in the sequence that they appear in the DOM across the pages. Users can also access lists, links, graphics, tables, forms, and other elements within an iframe.

## The heading hierarchy of an iframe SHOULD be designed to fit within the heading hierarchy of the parent document, if possible.

If you have control over the content of the embedded document in the iframe, the best practice is to fit the iframe heading hierarchy into the proper place within the existing heading hierarchy of the parent page. If the parent document is structured with a single `<h1>` at the top of the content (this is a recommended best practice), the `<iframe>` ought to take this into account, and not start with another `<h1>`. The `<iframe>` document ought to start with `<h2>` if the content is a direct child of the first heading on the page, or if it is a child of a level 2 heading, then the first heading of the iframe should be `<h3>`, and so on.

When iframes contain content from third-party web sites — as is often the case — it is not always possible to control the heading hierarchy. Because of the lack of control in these situations, the guidelines don't strictly require the heading hierarchies of the two documents to match, but it would still be better if they did.
