# Complex Text Alternatives

## Overview

Complex `<canvas>` elements like bar graphs and pie charts require a full text alternative of all the text and data presented in the complex image. ARIA role="img" designates the `<canvas>` as an image for the screen reader, and an accessible name can be created with an aria-label string value or an aria-labelledby ID reference to other strings in the DOM. The image can also have an accessible description via aria-describedby ID reference to text in the DOM.

Text alternatives for complex image data can also be presented as an accessible data table.

## All `<canvas>` elements used as complex images MUST have a detailed text alternative.

A `<canvas>` element will always require a text alternative, but that text alternative should be relatively brief. A limit of approximately 150 characters is best practice, because screen readers read aria-label and aria-labelledby as a single string of text, without allowing users to pause the screen reader and resume in the same place. Once the user pauses the screen reader, the user would need to back up then focus on the `<canvas>` element again to hear the label.

If the description requires more than about 150 characters, it should be represented in a different way, such as a long description or table below the `<canvas>` element.

### Example: `aria-label`

```html
<canvas id="can3" height="400" width="650" role="img" 
  aria-label="Bar Chart Values in Millions from 0 to 12000.
  Human: 11000, Chimp: 6200, Dolphin: 5800, Cat: 300"> 
</canvas>
```

### Example: `<canvas>` with text alternative via data table

```html
<canvas id="can2" height="400" width="650" role="img" aria-describedby="table1">
   Bar chart showing number of neurons in the cerebral cortex.
   The table below contains data details.
</canvas>
<table id="table1">
   <caption>Neurons in Cerebral Cortex</caption>
   <tbody>
     <tr>
       <th scope="col">Value</th>
       <th scope="col">Human</th>
       <th scope="col">Chimp</th>
       <th scope="col">Dolphin</th>
       <th scope="col">Cat</th>
     </tr>
     <tr>
       <th scope="row">Millions</th>
       <td>11000</td>
       <td>6200</td>
       <td>5800</td>
       <td>300</td>
     </tr>
   </tbody>
</table>
```