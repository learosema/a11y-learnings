# Responsive tables

## Tables SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.

As the viewport size changes, ensure that tables resize accordingly so they do not require horizontal scrolling. For tables with only a small number of columns and limited text, this may be accomplished simply by defining column widths as a percentage of the viewport width and constraining the maximum table width using max-width:100% on the table style. Accommodating larger tables in small viewports such as phones may require transforming and reorganizing the table into one column.