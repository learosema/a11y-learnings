# Decorative or redundant images

## Images that do not convey content, are decorative, or are redundant to content that is already conveyed in text MUST be given null alternative text (`alt=""`), ARIA role="presentation", or implemented as CSS backgrounds.

Provide "null" alt attributes (using `alt=""`) for images that do not provide information or do not require alternative text because the image is described in the page content.

Some developers will mistakenly leave off the alt attribute altogether on images that they deem do not need alternatives. This is not helpful to assistive technology users because the screen reader will often read the source attribute (i.e., file name) as the alternative text. To tell assistive technology to ignore an image, use a "blank alternative text" attribute: `alt=""`.

### Example

```html
<a href="https://dequeuniversity.com">
 <img src="home-icon.png" width="24" height="25" alt=""> 
 Home Page
</a>
```
