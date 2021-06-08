# Simple Text alternatives

## When `<canvas>` elements are used to display graphics, they MUST be assigned role="img".

The `<canvas>` element is not automatically treated as an image by screen readers. If the content inside the `<canvas>` element is intended to act as an image, it needs to be designated as such by assigning role="img" to it.

```html
<canvas id="canvasAsImage" role="img" width="400" height="100" 
aria-label="Canvas element marked as an image">
</canvas>
```

## All `<canvas>` elements MUST have a text alternative.

The `<canvas>` element encapsulates the object inside it and does not render the content in the DOM or in the accessibility tree via the accessibility API. Either internal fallback content or ARIA semantics must be used to create a text alternative accessible to screen readers.

### Option 1: `aria-label`

```html
<canvas id="goodCanvas1" width="700" height="100" role="img"
    aria-label="A red and white circular target with an arrow  
    pointing to the center of the target">
</canvas>
```

### Option 2: `aria-labelledby` pointing to fallback content inside the canvas element

```html
<canvas id="goodCanvas2" width="700" height="100" role="img"
    aria-labelledby="goodCanvas2Fallback" style="margin:auto">
    <p id="goodCanvas2Fallback">A red and white circular target with an arrow  
    pointing to the center of the target</p>
</canvas>
```

## The alternative text for `<canvas>` elements MUST be meaningful.

The alternative text must describe the image in a way that will be useful to blind users. In essence, the alternative text must serve as a substitute for the image, so that the meaning or purpose of the image is effectively communicated via the alternative text.

### Bad example

```html
<canvas id="badCanvas2" width="400" height="100">
    Your browser does not support the canvas element.
</canvas>
```
