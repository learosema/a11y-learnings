# Nested or Split tables

## Data table headers and data associations MUST NOT be referenced across nested, merged, or separate tables.

Nested data tables are data tables which exist inside other data tables. Nested data tables break the accessibility of the data presentation as a whole, making it impossible to associate the data and header cells appropriately with any of the standard methods. The scope method will not work properly, and neither will the id + headers method. If you really want to bend the rules, you could use aria-labelledby, but that would be a convoluted way to compensate for a poorly-designed table.