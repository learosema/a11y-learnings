# Complex Images

## Complex images MUST be briefly described using alt text AND MUST have a more complete long description.
Even if you've correctly associated visual labels with visual data in a graph or chart, blind users won’t be able to easily make sense of the graphics unless you provide a detailed text description of them. You could add all of the description to the alt text, but alt text is meant to be somewhat brief, no more than roughly 150 characters or so. From a technical standpoint, alt text can be much longer than 150 characters; however, from a practical standpoint, the convention is for alt text to be short. If 150 characters or so is insufficient to describe an image, you must use another method.

There are several ways of providing a long description for images:

- Provide the long description in the context of the HTML document itself.
- Provide a button that expands a collapsed region that contains the long description.
- Provide a button to open a dialog that contains the long description.
- Provide a link to a long description on another page via a normal link text.
- Provide a link to a long description on another page via the longdesc attribute.

No matter which method you choose, you still need to provide a brief alt text describing the main purpose or content of the image.

### Example

```html
<img class="border" src="bar-chart.png" width="546" height="330" 
alt="Bar chart with percentages. Extended description below chart."
aria-describedby="description-extended">

<div id="description-extended">
    <p>Full long description goes here.</p>
</div>
```

## The long description (or a link or button to access the long description) SHOULD be visible to sighted users.

Some complex images may be too complex for sighted users. So, some sighted users may benefit from having access to a detailed description of a complex image. If the description is provided through the longdesc attribute, sighted users will not be able to access the text-based details about the image.

## The long description SHOULD be programmatically associated with the image.

The extended alternative description for a complex image can be accessible to screen reader users through the longdesc or aria-describedby attributes. Take note, though, that the longdesc method is only available to screen reader users. Other methods like providing a link or including the description in the document are available to both screen reader users and users who do not use screen readers.

### Example

```html
<img class="border" src="bar-chart.png" width="546" height="330" 
alt="Bar chart with percentages" aria-describedby="squirrelchart">
  
<h3>The Squirrels</h3>
<div id="squirrelchart">
  <p>Last year, Josephine kept track of the number of times ...</p>
</div>
```
