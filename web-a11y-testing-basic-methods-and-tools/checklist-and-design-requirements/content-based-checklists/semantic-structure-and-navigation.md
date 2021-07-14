# Semantic Structure and Navigation: Summary & Checklist

Screen readers and other assistive technologies rely on the underlying semantic markup to convey meaningful information about the structure and content of web pages. The following is a list of all of the main principles covered in this module:

## Page Title

### Title for Every Page

- The page `<title>` MUST be present and MUST contain text.
- The page `<title>` MUST be updated when the web address changes.

### Meaningful Page Title

- The page `<title>` MUST be accurate and informative.
- If a page is the result of a user action or scripted change of context, the text of the `<title>` SHOULD describe the result or change of context to the user.
- The `<title>` SHOULD be concise.
- The page `<title>` SHOULD be unique, if possible.
- Unique information SHOULD come first in the `<title>`.
- The page `<title>` SHOULD match (or be very similar to) the top heading in the main content.

## Language

### Primary Language of Page

- The primary language of the page MUST be identified accurately on the `<html>` element.
- The primary language of the page MUST be identified with a valid value on the `<html>` element.

### Language of Parts within the Page

- Inline language changes MUST be identified with a valid lang attribute.

### Language Codes

- The language code MUST be valid.

## Landmarks

### Creating Landmarks (HTML 5, ARIA)

- Landmarks SHOULD be used to designate pre-defined parts of the layout (`<header>`, `<nav>`, `<main>`, `<footer>`, etc.).

### Best Practices for Landmarks

- All text SHOULD be contained within a landmark region.
- Multiple instances of the same type of landmark SHOULD be distinguishable by different determinable labels (aria-label or aria-labelledby).
- A page SHOULD NOT contain more than one instance of each of the following landmarks: banner, main, and contentinfo.
- The total number of landmarks SHOULD be minimized to the extent appropriate for the content.

### Backward Compatibility

- Landmarks SHOULD be made backward compatible.

## General UI Components

- In content implemented using markup languages, the purpose of User Interface Components, icons, and regions MAY be programmatically determinable.

## Headings

### Real Headings

- Text that acts as a heading visually or structurally SHOULD be designated as a true heading in the markup.
- Text that does not act as a heading visually or structurally SHOULD NOT be marked as a heading.

### Meaningful Text

- Headings MUST be accurate and informative.
- Heading text SHOULD be concise and relatively brief.

### Outline/Hierarchy of Content

- Headings SHOULD convey a clear and accurate structural outline of the sections of content of a web page.
- Headings SHOULD NOT skip hierarchical levels.

### Heading Level 1 Best Practices

- The beginning of the main content SHOULD start with `<h1>`.
- Most web pages SHOULD have only one `<h1>`.

## Links

### Designate Links Correctly

- Links MUST be semantically designated as such.
- Links and buttons SHOULD be designated semantically according to their functions.

### Link Text

- A link MUST have programmatically determinable text, as determined by the accessible name calculation algorithm.
- The purpose of each link SHOULD be able to be determined from the link text alone.
- The link text SHOULD NOT repeat the role ("link").
- Features such as labels, names, and text alternatives for content that has the same functionality across multiple web pages MUST be consistently identified.

### Links to External Sites, New Windows, Files

-A link that opens in a new window or tab SHOULD indicate that it opens in a new window or tab.

- A link to a file or destination in an alternative or non-web format SHOULD indicate the file or destination type.
- A link to an external site MAY indicate that it leads to an external site.

### Visually Distinguishable from Text

- Links MUST be visually distinguishable from surrounding text.

### Visual focus indicator

- All focusable elements MUST have a visual focus indicator when in focus.
- Focusable elements SHOULD have enhanced visual focus indicator styles.

## Navigation Between Pages

### Navigation Lists

- A navigation list SHOULD be designated with the `<nav>` element or role="navigation".
- A navigation list SHOULD include a visible method of informing users which page within the navigation list is the currently active/visible page.
- A navigation list SHOULD include a method of informing blind users which page within the navigation list is the currently active/visible page.

### Consistency

- Navigation patterns that are repeated on web pages MUST be presented in the same relative order each time they appear and MUST NOT change order when navigating through the site.

## Navigation Within Pages

### Skip Navigation Links

- A keyboard-functional "skip" link SHOULD be provided to allow keyboard users to navigate directly to the main content.
- The "skip link" SHOULD be the first focusable element on the page.
- A skip link MUST be either visible at all times or visible on keyboard focus.

### Table of Contents

- A table of contents for the page MAY be included at the top of the content or in the header.
- If a table of contents for the page is included, it SHOULD reflect the heading structure of the page.

### Reading Order and Tab/Focus Order

- The reading order MUST be logical and intuitive.
- The navigation order of focusable elements MUST be logical and intuitive.
- tabindex of positive values SHOULD NOT be used.

### Paginated Views

- A paginated view SHOULD include a visible method of informing users which view is the currently active/visible view.
- A paginated view SHOULD include a method of informing blind users which view is the currently active/visible view.

### Single-Key Shortcuts

- If a single-character-key shortcut exists, then at least one of the following MUST be true: single-character-key shortcuts can be turned off, remapped, or are only active when the relevant user interface component is in focus.

## Tables

### Semantic Markup for Tabular Data

- Tabular data SHOULD be represented in a `<table>`.

### Table caption/name

- Data tables SHOULD have a programmatically-associated caption or name.
- The name/caption of a data table SHOULD describe the identity or purpose of the table accurately, meaningfully, and succinctly.
- The name/caption of each data table SHOULD be unique within the context of other tables on the same page.

### Table Headers

- Table headers MUST be designated with `<th>`.
- Data table header text MUST accurately describe the category of the corresponding data cells.

### Simple Header Associations

- Table data cells MUST be associated with their corresponding header cells.

### Grouped Header Associations

- Table data group headers MUST be associated with their corresponding data cell groups.

### Complex Header Associations

- Header/data associations that cannot be designated with `<th>` and scope MUST be designated with headers plus id.

### Nested or Split Tables

- Data table headers and data associations MUST NOT be referenced across nested, merged, or separate tables.

### Table Summary

- A summary MAY be provided for data tables.
- A data table summary, if provided, SHOULD make the table more understandable to screen reader users.

### Layout Tables

- Tables SHOULD NOT be used for the purpose of purely visual (non-data) layout.
- Layout tables MUST NOT contain data table markup.

## Lists

### Semantic Markup for Lists

- Lists MUST be constructed using the appropriate semantic markup.

## Iframes

### Frame titles

- Iframes that convey content to users MUST have a non-empty title attribute.
- The iframe title MUST be accurate and descriptive.
- Frames MUST have a unique title (in the context of the page).

### Page Title Within an Iframe

- The source page of an iframe MUST have a valid, meaningful `<title>`.

### Semantic structure across iframes

- The heading hierarchy of an iframe SHOULD be designed to fit within the heading hierarchy of the parent document, if possible.
- Hiding iframes that don't contain meaningful content
- Hidden frames or frames that do not convey content to users SHOULD be hidden from assistive technologies using aria-hidden="true".

## Other Semantic Elements

### `<strong>` and `<em>`

- Critical emphasis in the text SHOULD be conveyed through visual styling.
- Critical emphasis in the text SHOULD be conveyed in a text-based format.

### `<blockquote>` and `<q>`

- The `<blockquote>` element SHOULD be used to designate long (block level) quotations.
- The `<blockquote>` element SHOULD NOT be used for visual styling alone.
- The `<q>` element (for inline quotations) SHOULD NOT be used as the only way to designate quotations.

### `<code>`, `<pre>`

- Code SHOULD be marked with the `<code>` element.
- Blocks of code SHOULD be formatted with the `<pre>` element.

### Strikethrough/Delete and Insert

- Strikethrough text SHOULD be marked with the `<del>` element.
- Critical strikethrough text MUST be supplemented with a text-based method to convey the meaning of the strikethrough.
- Text designated for insertion SHOULD be marked with the `<ins>` element.
- Critical text designated for insertion MUST be supplemented with a text-based method to convey the meaning of the insertion.

### Highlighting (`<mark>`)

- Highlighted text SHOULD be marked with the `<mark>` element.
- Critical highlighted text SHOULD be supplemented with a text-based method to convey the meaning of the highlighting.

## Parsing and Validity

### Complete Start and End Tags

- In content implemented using markup languages, elements MUST have complete start and end tags.

### Conflicts and duplicates

- IDs MUST be unique within a web page.
- Names, when provided, of block level elements (e.g. landmarks, tables, iframes, etc.) SHOULD be unique within a web page.

### Parent-child relationships

- Markup SHOULD adhere to required parent-child relationships of elements and attributes.

### Deprecated Markup

- Deprecated markup SHOULD NOT be used.
