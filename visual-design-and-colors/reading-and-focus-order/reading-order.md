# Reading order

## The reading order MUST be logical and intuitive.

If the reading order is illogical or unintuitive, the content will not make sense, or it will be difficult to understand.

Screen readers ignore all of the CSS layout in your web design. Turning off the style sheets is one way to check the reading order of static content. When the content is stripped bare of the visual styling like this, it is sort of how a screen reader "sees" it.

### Example

```html

<div class="overallContainer">
  <div class="columnsContainer">
    <div class="disabilityTypesColumn">
      <p><strong>1. Disability Types:</strong></p>
      <ul>
        <li>Visual</li>
        <li>Auditory</li>
        <li>Motor</li>
        <li>Cognitive</li>
        <li>Seizures</li>
      </ul>
    </div>
    <div class="atColumn">
      <p><strong>2. Assistive Technologies: </strong></p>
      <ul>
        <li>Screen readers</li>
        <li>Screen enlargers</li>
        <li>Mouth stick</li>
        <li>Eye-gaze tracking</li>
        <li>etc.</li>
      </ul>
    </div>
    <div class="classesColumn">
      <p><strong>3. Classes:</strong></p>
      <ul>
        <li>Web Accessibility Fundamentals</li>
        <li>HTML/CSS Accessibility</li>
        <li>Web Accessibility Testing</li>
        <li>and more!</li>
      </ul>
    </div>
  </div>
    <div class="footerSection">
      <p><strong>4. </strong>Accessible design is good design.</p>
    </div>
</div>
```

```css
.overallContainer {
	height:25em;
	font-size: 1em;
}

.columnsContainer {
	display: block;
	clear: both;
	margin-bottom: 5px; 
	width:750px;
}

.columnsContainer div {
	float: left;
	width: 200px;
	height: 18em;
	padding: 4px;
	border: 1px dotted gray; }

.disabilityTypesColumn { 
	margin-right: 4px;
	background:#fff;
}

.atColumn {
	margin-right: 4px;
	background:#fff;
}

.classesColumn {
	clear: right;
	background:#fff;
}

.footerSection {
	display:block; 
	clear: both;
	margin-top: 4px;
	height:3em;
	width:640px;
	padding:4px;
	border: 1px dotted gray;
	background:#fff;	
}
```

