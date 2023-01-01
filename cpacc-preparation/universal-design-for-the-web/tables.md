# Tables

## Associate Data Cells with Header Cells

<figure><figcaption><h3>Data Tables</h3></figcaption>
Associate data cells with header cells to allow screen reader users to navigate effectively within tables.
</figure>

Tables are a visual way of organizing data. They present information in a two-dimensional grid, with one or more header cells visually associated with each data cell by being placed either at the top of the column or at the beginning of a row. Blind users can't see this visual organization, though, so you have to make the association explicit between data cells and header cells.

Without an explicit association between header cells and data cells, screen readers will just read the content of the data cell without giving it any context or letting users know what the cell represents. If you mark up a table correctly, the screen reader will read the header cells before each data cell when navigating through the data cells.

## Good Example

In this simple table below, the headers have been associated with the data cells. As screen reader users move through the first row of data cells, the screen reader will read the corresponding header cell, then read the data cell.

Table: Number of candies in children's bags, by day of week

 	       | Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday
---------|--------|--------|---------|-----------|----------|--------|----------
Jeremiah | 84     | 78	   | 56      | 42        | 23       | 15     | 0
Anne     | 125    | 124    | 112     | 95        | 95       | 95     | 80
John     | 53     | 42     | 21      | 2         | 0        | 0      | 0

If you read the second row of the table above with a screen reader, navigating from cell to cell, the screen reader will say:

  "Jeremiah, Sunday 84, Monday 78, Tuesday 56, Wednesday 42, Thursday 23, Friday 15, Saturday 0."

If you don't mark the headers appropriately, the screen reader will say:

 "Jeremiah, 84, 78, 56, 42, 23, 15, 0."

As you go through the days of the week, you may lose track of which day you're on. Was 42 for Wednesday, or was it for Thursday? It's easy to forget. With larger or more complex tables, this is an even greater problem.

The markup for this table, for those who are curious, is shown below. The important parts are:

The header cells are marked with <th>.
The scope of the header cells is defined as either row or col, for column.

```html
<table class="data">
<caption>Number of candies in children's bags, by day of week</caption>
<tr>
    <td>&nbsp;</td>
    <th scope="col">Sunday</th>
    <th scope="col">Monday</th>
    <th scope="col">Tuesday</th>
    <th scope="col">Wednesday</th>
    <th scope="col">Thursday</th>
    <th scope="col">Friday</th>
    <th scope="col">Saturday</th>
</tr>
<tr>
    <th scope="row">Jeremiah</th>
    <td>84</td>
    <td>78</td>
    <td>56</td>
    <td>42</td>
    <td>23</td>
    <td>15</td>
    <td>0</td>
</tr>
<tr>
    <th scope="row">Anne</th>
    <td>125</td>
    <td>124</td>
    <td>112</td>
    <td>95</td>
    <td>95</td>
    <td>95</td>
    <td>80</td>
</tr>
<tr>
    <th scope="row">John</th>
    <td>53</td>
    <td>42</td>
    <td>21</td>
    <td>2</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    </tr>
</table>
```

There are additional nuances when it comes to coding tables for accessibility, but these are the basics. Deque's HTML and CSS Accessibility course covers those nuances in more detail.
