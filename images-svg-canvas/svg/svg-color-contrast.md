# SVG Color Contrast

## SVG images SHOULD include a base background color behind the important parts of the image, at a minimum.

If an SVG image does not have a background color set, the background color of the image itself will change when the user switches into Windows High Contrast Mode. 

That may or may not be a problem for a given image, but if large portions of the SVG image are transparent, and if they depend on a particular background color on the web page to look correct, the SVG image will probably be difficult to discern when the background color changes.

### Note

It is not necessary to completely fill the background rectangle of an SVG image. Parts of the SVG image can remain transparent as long as there are no transparent parts within the SVG that would cause the image to become difficult to understand if those colors were to change.

For example, if the assumption is that the background color of the page is white, and if parts of the SVG image are white only because the color of the web page is showing through, those parts of the image will turn black if the user switches to Windows High Contrast Mode with a black background.

The background fill can be any shape, as long as it fills in the important parts of the image.


## SVG images SHOULD be styled to ensure compatibility with Windows High Contrast Mode

SVG images will retain their colors when the user switches into Windows High Contrast Mode.

Some SVG images will naturally look fine in Windows High Contrast Mode, so there is no need to create specific styles for them. In other cases, SVG images will not have the proper contrast in comparison with the background. This is especially true when CSS is used to style SVG image components. Windows High Contrast Mode overrides CSS colors, which can drastically change the look of the image (as well as the entire page around the image).

If the SVG image is problematic in Windows High Contrast Mode, one solution is to detect when Windows High Contrast Mode is being used and customize the styling of the SVG image accordingly. There are two basic approaches to detecting Windows High Contrast Mode:

- Use proprietary CSS media queries (Edge and Internet Explorer only)
- Use JavaScript to detect user-initiated changes to colors (the changes may be at the browser level or at the operating system level)

JavaScript tests are required for browsers other than Edge and Internet Explorer. This method can be more robust than the media detection method mentioned above and can take into account other high contrast software or user-specific styles.

Script for detecting Windows High Contrast Mode:

- [Windows High Contrast Mode detection script by Hans Hillen](http://jsfiddle.net/karlgroves/XR8Su/6/)
- [Explanation of the script's methods and philosophy](http://hanshillen.github.io/HCMDS/hcmode_detection.html)

### Example: 

This method will work in Edge and Internet Explorer, but not in other browsers.

Note: [`-ms-high-contrast: none`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/-ms-high-contrast) no longer supported in Edge 18 and Chromium-based Edge. 
Use [`forced-colors`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/forced-colors) instead.


```html
/* Styles for all high contrast modes: */
@media screen and (-ms-high-contrast: active) { }

/* Styles for the Windows "High Contrast Black" theme: */
@media screen and (-ms-high-contrast: white-on-black) { }

/* Styles for the windows "High Contrast White" theme: */
@media screen and (-ms-high-contrast: black-on-white) { }
```
