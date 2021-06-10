# Responsive images

## Images SHOULD reflow to fill most of the width of the viewport, without causing any horizontal viewport overflow.

As the viewport size changes, ensure that images are resized in such a way as to not require horizontal scrolling. This can be accomplished by various methods including:

- max-width style in the CSS
- the srcset attribute on the `<img>` element
- `<picture>` element with multiple `<source>`s with explicit media attributes

### Example

Make sure images are visible on small screens and prevent horizontal scrolling using max-width:100%.

```css
@media (max-width: 320px) {
    main img {
    max-width: 100%;
    height: auto;
    }
}
```

### Example with `<picture>` element and media queries

```html
<picture> 		
    <source 		
        media="(min-width: 40em)" 		
        srcset="
            large.png   900w, 		        
            medium.png  600w, 		        
            small.png   400w" /> 	
    <source 		
        srcset="
            small.png" /> 	
    <img src="medium.png" 
        alt="Wheelchair racers in the Paralympics speed down the track" /> 
</picture>
```
