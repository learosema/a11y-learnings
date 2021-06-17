# Tab Order

## The navigation order of focusable elements MUST be logical and intuitive.

When keyboard users tab through the focusable items (buttons, links, form elements, custom controls, etc.), the order needs to make sense, so they don't get confused.

If a keyboard user—whether sighted or blind—uses the tab key to go through all of the focusable elements (links, buttons, form elements, etc.), the browser will start with the focusable elements at the top and proceed linearly through all the focusable elements until reaching the bottom.

The browser ignores all of the visual formatting—columns, floating elements, margin, padding, positioning, etc.—and pays attention to the underlying order that things appear in the DOM.

Visual users will expect the tab order to start in the upper left (Disability Types), go through the list of links in the left column, then go through the links in the middle column (Assistive Technologies), then the links in the column on the right (Classes), then the link on the bottom ("Accessible design is good design").

Unfortunately, the tab order does not follow the expected sequence. The tab order starts in the right column, then goes to the footer at the bottom, then to the left column, then the middle column. In this example, the reason everything is so out of order is because CSS absolute positioning was used, and the person who created the content didn't update the order in the source code to match the visual order.

Here is the HTML source code followed by the CSS code for this example.

```html
<div class="overallContainer2">
    <div class="columnsContainer2">
      <div class="classesColumn2">
          <!-- The following section is first in the DOM, but it should be third -->
        <p><strong>3. Classes:</strong></p>
        <ul>
          <li><a href="#">Web Accessibility Fundamentals</a></li>
          <li><a href="#">HTML/CSS Accessibility</a></li>
          <li><a href="#">Web Accessibility Testing</a></li>
          <li><a href="#">and more!</a></li>
        </ul>
      </div>
      <div class="footerSection2">
          <!-- The following section is second in the DOM, but it should be fourth -->
        <p><strong>4. </strong><a href="#">Accessible design is good design.</a></p>
      </div>
      <div class="disabilityTypesColumn2">
          <!-- The following section is third in the DOM, but it should be first -->
        <p><strong>1. Disability Types:</strong></p>
        <ul>
          <li><a href="#">Visual</a></li>
          <li><a href="#">Auditory</a></li>
          <li><a href="#">Motor</a></li>
          <li><a href="#">Cognitive</a></li>
          <li><a href="#">Seizures</a></li>
        </ul>
      </div>
      <div class="atColumn2">
          <!-- The following section is fourth in the DOM, but it should be second -->
        <p><strong>2. Assistive Technologies: </strong></p>
        <ul>
          <li><a href="#">Screen readers</a></li>
          <li><a href="#">Screen enlargers</a></li>
          <li><a href="#">Mouth stick</a></li>
          <li><a href="#">Eye-gaze tracking</a></li>
          <li><a href="#">etc.</a></li>
        </ul>
      </div>
    </div>
</div>
```

```css
.overallContainer2 {
	height:25em;
	font-size:13px;
}

.columnsContainer2 {
	position:absolute;
	height:25em;
	width:750px;
}

.disabilityTypesColumn2 {
	position:absolute;
	left:10px;
	top:10px;
	width:200px;
	height:18em;
	padding:4px;
	border:dotted gray 1px;
	background:#fff;
}

.atColumn2 {
	position:absolute;
	left:230px;
	top:10px;
	height:18em;
	width:200px;
	padding:4px;
	border:dotted gray 1px;
	background:#fff;
}

.classesColumn2 {
	position:absolute;
	left:450px;
	top:10px;
	height:18em;
	width:200px;
	padding:4px;
	border:dotted gray 1px;
	background:#fff;
}

.footerSection2 {
	position:absolute;
	left:10px;
	top:20em;
	height:3em;
	width:640px;
	padding:4px;
	border:dotted gray 1px;
	background:#fff;	
}
```

## tabindex of positive values SHOULD NOT be used.

It is possible to customize the tab order of focusable items using tabindex, by setting it to numerical values like 1, 2, 3, etc., but this has the potential to cause significant problems for keyboard users.

- It causes a discrepancy between the tab order and the reading order, leading to confusion when interacting with the page using a keyboard
- It removes the items from their natural tab order, and instead places them first in the tab order. Anything with any tabindex value of 1 or greater will come before all other focusable items. For example, if only one item on the page has a tabindex set, and it's set to 9000, that item will be the first thing a user tabs to, even though the number is very large. When tabbing away from the item with tabindex="9000", the focus will next go to the first focusable item in the DOM. If the user continues tabbing through the web page, the user will eventually arrive at the place where the tabindex="9000" item is and will expect to be able to tab to it, but will not be able to, because the item's position in the DOM does not correspond to the item's tab order. The user would have already tabbed to it previously, so the browser skips over that item. It's confusing to the user—especially sighted keyboard users—when this happens.