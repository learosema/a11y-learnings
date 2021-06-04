# Table Headers

## Table headers MUST be designated with <th>.

The only way that screen readers can know if a table cell is a header is by marking it with <th>. Otherwise screen readers may assume the table is just for visual formatting and will not read the header information as they should.

If the header cells are on the first row, screen readers will assume that they all apply to the columns below (in other words, there is an implicit `scope="col"`. It still is a good idea to make the scope explicit by adding a scope of one of the following: `col`, `row`, `colgroup`, or `rowgroup`.

## Data table header text MUST accurately describe the category of the corresponding data cells.

If the text in the header cell is vague (for example, naming it "Column 2"), or if it contains extraneous information (like links, buttons or extra descriptions that aren't the name of the column), it can be confusing for screen reader users. It's best to keep the header text accurate and simple.