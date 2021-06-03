# Backward compatibility

## Landmarks SHOULD be made backward compatible.

If you plan to support older browsers that don't understand HTML 5 elements, you'll need to take some extra steps to ensure the HTML 5 elements render correctly visually and in the DOM.

```css
/* landmarks */
article, aside, footer, header, main, nav, section,

/* other HTML 5 elements that should (probably) 
be set to display:block */
audio, canvas, datalist, details, figcaption, 
figure, output, progress, summary, video {
   display:block;
}

```
