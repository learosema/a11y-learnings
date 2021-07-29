# Table Mode

## Multi-directional navigation

Screen readers allow users to navigate through tables in any direction: right, down, left, and up. When using the proper keystrokes, the experience is much like navigating through the cells in a spreadsheet. All Windows screen readers use Control + Alt + Arrow keys for table navigation; on macOS it is Control + Option + Arrow keys.

## Table headers

While navigating from cell to cell, the screen reader will read the table headers (if any) for that cell. The headers may be row headers, column headers, rowgroup headers, or colgroup headers. If the screen reader reads only the contents of the cell, it probably means the markup in the data table is not correct.

### Note:

Screen readers typically only read the new header information. If you navigate across a row, the screen reader will read the row header on the first cell, but not on the subsequent cells. It will read the relevant column headers though, because those represent new information. So if you hear it read only one of the headers when you think it should read two, that's probably the reason (unless you didn't mark both headers correctly in the HTML).
