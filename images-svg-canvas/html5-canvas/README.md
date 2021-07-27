# HTML5 Canvas

## Introduction

The `<canvas>` element renders as pixels on the screen that do not scale like SVG. JavaScript is used to dynamically draw on the `<canvas>` element at runtime which allows creation of dynamic images like charts and graphs. The `<canvas>` element is often used for HTML5 desktop and mobile game development.

The `<canvas>` element has support in all browsers and will render on-screen, but the `<canvas>` element's content will not be accessible to screen readers. With the `<canvas>` element, accessibility has to be added with JavaScript or ARIA on the `<canvas>` element itself or using internal fallback content placed within the opening and closing `<canvas>` tags. Content in the `<canvas>` element is not part of the DOM except for the fallback content.

SVG is a better choice than `<canvas>` for interactive content and custom controls because SVG has internal accessibility semantics and the ability to easily add interactivity with JavaScript.

The `<canvas>` element should not be used to generate text, because it renders as an image of text that pixelates when enlarged and cannot be customized by the user like CSS text.

The `<canvas>` element must have an accessible name and description that matches the visible text and content inside the canvas drawing area.

When the `<canvas>` element is used as mouse and keyboard operable custom UI controls, it must have an accessibility role, e.g., role="button" for custom `<canvas>` buttons.

References:

- [The Canvas Shadow dom](<https://msdn.microsoft.com/en-us/library/hh968259(v=vs.85).aspx>)
- [User input in canvas-based games](https://developer.ibm.com/industries/gaming/tutorials/wa-games/)

## In this Section:

- [Simple Text Alternatives](simple-text-alternatives.md)
- [Complex Text Alternatives](complex-text-alternatives.md)
- [Low Vision Accessibility](low-vision-a11y.md)
- [Keyboard Accessibility](keyboard-a11y.md)
