# Complex Header Associations

## Header/data associations that cannot be designated with `<th>` and scope MUST be designated with headers plus id

Tables with a complex structure — in which data cells are merged or there are more than two levels of headers for any given dimension — require a different technique than simply marking the header cells with a scope of col, row, colgroup, or rowgroup. Each data cell must be explicitly associated with each corresponding header cell using headers and id.

### Warning

Complex table structures with irregular column or row designations are difficult for screen reader users to understand and navigate even when all the markup is "perfect" for accessibility compliance. It is much better to create a simple table with no spanned cells than to create a confusing complex table that technically passes the accessibility guidelines.

Some screen readers, especially on mobile devices, do not support accessibility complex table markup. 

### Note: Old versions of VoiceOver did not support the id + headers method

Up until Mac OS X 10.10.2, VoiceOver did not support the ability to read table headers with the id + headers method. Some versions even read the wrong headers with the data cells. Fortunately, the current version of VoiceOver does read the data and header associations correctly.

### Example

```html
<table class="complexexample">
  <caption>New Employee Orientation Schedule</caption>
  <tbody>
    <tr>
      <th rowspan="2" id="date">Date</th>
      <th colspan="2" id="schedule">Schedule</th>
      <th rowspan="2" id="location">Location</th>
      <th colspan="2" rowspan="2" id="topics1">Topics</th>
    </tr>
    <tr>
      <th id="start">Start</th>
      <th id="end">End</th>
    </tr>
    <tr>
      <th id="monday" rowspan="5">Monday, June 1</th>
      <td headers="schedule start monday">9:00 a.m.</td>
      <td headers="schedule end monday">10:30 a.m.</td>
      <td headers="location monday">RH 001</td>
      <td headers="topics1 monday">
        Introduction to Company: Vision and Mission</td>
    </tr>
    <tr>
      <td headers="schedule start monday">10:30 a.m.</td>
      <td headers="schedule end monday">12:00 p.m.</td>
      <td headers="location monday">RH 001</td>
      <td headers="topics1 monday">HR Policies Review</td>
    </tr>
    <tr>
      <td headers="schedule monday" colspan="5">
        <strong><em>
          Lunch from 12:00 p.m. to 1:00 p.m.
        </em></strong>
      </td>
    </tr>
    <tr>
      <td headers="schedule start monday">1:00 p.m.</td> 
      <td headers="schedule end monday">2:30 p.m.</td>
      <td headers="location monday">RH 001</td>
      <td headers="topics1 monday">Overview of Benefits</td>
    </tr>
    <tr>
      <td headers="schedule start monday">3:00 p.m.</td>
      <td headers="schedule end monday">4:30 p.m.</td>
      <td headers="location monday">RH 005</td>
      <td headers="topics1 monday">
        Health and Safety Procedures
      </td>
    </tr>
  </tbody>
</table>
```