# Conflicts and duplicates

## IDs MUST be unique within a web page.

Invalid code doesn't always cause accessibility problems, but it can, especially if there are errors in the parts of the markup that screen readers rely on to communicate the semantics of the web page to users.

Screen readers rely on IDs in the markup for a variety of things, including:

- form labels (using `<label>` and the id attribute on the form field)
- table header associations (when using the headers plus id method)
- labels for custom JavaScript/ARIA widgets (when using aria-labelledby)
- descriptions for custom JavaScript/ARIA widgets (when using aria-describedby)
- other associations for custom JavaScript/ARIA widgets (using attributes like aria-controls, aria-owns, etc.)

If there are two elements on the same page with the same ID, screen readers may read the information incorrectly (like reading the wrong label with a text input), which can cause screen reader users to input the wrong information, or at a minimum to be confused.

## Names, when provided, of block level elements (e.g. landmarks, tables, iframes, etc.) SHOULD be unique within a web page.

Screen reader users have the ability to pull up lists of landmarks (e.g. navigation, sections, forms, etc.), tables, and other block level elements. To the extent possible, each element of the same type should be given a unique name, to allow users to distinguish them.

For example, if you have two tables that both have a `<caption>` of "Financial Results," screen reader users will not be able to tell the tables apart when they pull up the list of tables on the page.