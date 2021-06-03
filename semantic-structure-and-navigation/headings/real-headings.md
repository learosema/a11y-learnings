# Real headings

## Text that acts as a heading visually or structurally SHOULD be designated as a true heading in the markup.

Headings are about logical structure, not visual effects. Big bold text may look like a heading to visual users, but screen readers ignore the size and font-weight of the text, so blind users cannot know a phrase is a heading unless it is marked up in the HTML code as such, using `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, or `<h6>`. Even though the bad example below includes the same text and is styled to look similar in the browser to the good examples below, only the good examples create real headings that screen readers can use.

## Text that does not act as a heading visually or structurally SHOULD NOT be marked as a heading.

If you want to create big, bold text for non-heading text, use styles to achieve that effect. If you use heading markup (`<h1>`, `<h2>`, etc.) for non-heading text, you will confuse screen reader users by creating an inaccurate structural outline of the page contents.
