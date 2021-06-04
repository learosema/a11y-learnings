# Layout Tables

## Tables SHOULD NOT be used for the purpose of purely visual (non-data) layout.

Using tables for visual layout and not for data tables is discouraged but is technically allowed by accessibility guidelines. There is no severe accessibility consequence for using layout tables, but tables were designed for data grids, from a semantic structure perspective, so it is better to use them only for that purpose. Besides, CSS is a more robust way to design visual layouts for the modern web.

If a layout table must be used, `role="presentation"` should be added to the `<table>` element to ensure that screen readers will read the content of layout tables as text, rather than as a table (essentially ignoring the semantic table markup), and treat them kind of like div or `<p>` elements.

## Layout tables MUST NOT contain data table markup.

If a table is used strictly for visual layout purposes, don't include any of the header markup for data tables, because if you do, screen readers will inform users that a table is present, and users will expect the table to represent tabular data, which won't be accurate in layout tables.

Specifically, layout tables should avoid:

- The `<caption>` element
- The `<summary>` attribute
- The `<th>` element
- The scope attribute
- The headers attribute
