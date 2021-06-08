# Keyboard Accessibility

## Overview

Custom UI controls can be created as `<canvas>` elements with JavaScript event handling. A `<canvas>` element that is operable with the mouse must also work with the keyboard. Hover styles should match keyboard focus styles. Any `<canvas>` controls with onclick and onmousedown events must have keyboard events that check for Enter and Spacebar key activation.

## Accessible Name and Role

Standard ARIA methods to provide custom controls accessible names and roles works the same for canvas elements, for example, `<canvas role="button" aria-label="Accessible Name"></canvas>` speaks as "Accessible Name button".

Fallback content can also be used by placing a native button in the canvas tag and attaching the mouse behavior of the canvas button as keyboard events of the native button.

This allows keyboard users to tab to the button and it will have a native role and text value. Keyboard focus outline will not surround the canvas if fallback content is used, so a focus indicator would have to added.

## A <canvas> element operable with mouse MUST also be keyboard accessible.

### Keyboard Focusability

Use `tabindex="0"` to make a <canvas> element focusable in the default source code order when tabbing. Tabindex only makes the element tabbable, but it will not activate with Enter or Spacebar keys until the extra events are added.

### Keyboard Operability

The `<canvas>` element has no native keyboard operability, so onclick events will not be triggered by Enter or Spacebar keys. Add an onkeydown event that checks if the Enter or Spacebar keyCode keys are pressed then prevents the default behavior and fires the normal button code that was previously only mouse operable.

### Example: `<canvas>` buttons with focusability and accessible JavaScript keyboard events

```html
<canvas id="mycanvas" width="128" height="36" tabindex="0" 
    role="button" aria-label="Canvas button"
    onkeydown="if(event.keyCode==13 || event.keyCode==32){
       event.preventDefault(); 
       canvasDown(this)
    }"
    onkeyup="if(event.keyCode==13 || event.keyCode==32){
       event.preventDefault(); canvasUp(this)
    }"
    onmousedown="canvasDown(this)"  
    onmouseup="canvasUp(this)"
    onmouseover="canvasOver()" 
    onmouseout="canvasOut()"
    onfocus="canvasOver()" 
    onblur="canvasOut()"> 
</canvas>
```
