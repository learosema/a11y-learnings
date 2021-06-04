# Grouped Header Associations

## Table data group headers MUST be associated with their corresponding data cell groups.
When you merge table header cells, you need to designate one header as corresponding to multiple rows or columns. The easiest way is to use scope="rowgroup" or scope="colgroup". Screen readers will read the multiple headers when navigating through the tables.

### Note

Screen reader users will sometimes find table header groups somewhat confusing to navigate, even when they are marked up perfectly. If possible, create simpler tables that do not require any merged cells or header groups.

### Note

Screen reader support for `scope="rowgroup"` has historically been worse than support for `scope="colgroup"`, so for maximum accessibility, especially in terms of backward compatibility, it is best to orient the table in a configuration that allows `scope="colgroup"`, and which does not require `scope="rowgroup"`.


### Example

This table has multiple levels of column headers.

```html
<table class="data complex">
  <caption>
    Table with colgroup
  </caption>
  <thead>
    <tr>
      <td rowspan="2">&nbsp;</td>
      <th colspan="3" scope="colgroup">Females</th>
      <th colspan="3" scope="colgroup">Males</th>
    </tr>
    <tr>
      <th scope="col">Mary</th>
      <th scope="col">Betsy</th>
      <th scope="col">Joanne</th>
      <th scope="col">Matt</th>
      <th scope="col">Todd</th>
      <th scope="col">Jake</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1 mile</th>
      <td>8:32</td>
      <td>7:43</td>
      <td>9:51</td>
      <td>7:55</td>
      <td>7:01</td>
      <td>7:51</td>
    </tr>
    <tr>
      <th scope="row">5 km</th>
      <td>28:04</td>
      <td>26:47</td>
      <td>38:15</td>
      <td>27:27</td>
      <td>24:21</td>
      <td>24:31</td>
    </tr>
    <tr>
      <th scope="row">10 km</th>
      <td>1:01:16</td>
      <td>55:38</td>
      <td>1:56:01</td>
      <td>57:04</td>
      <td>50:35</td>
      <td>50:45</td>
    </tr>
  </tbody>
</table>
```