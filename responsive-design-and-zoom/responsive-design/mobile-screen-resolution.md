# Mobile Screen Resolution

## Mobile Viewports are Small

Mobile browsers have a much smaller viewport than desktop browsers. The iPhone up to and including iPhone 5s, for example, has a viewport of 320 pixels, compared with desktop/laptop monitors which allow the browser to fill the maximum width of the much larger screens. 

The available width of modern desktop/laptop monitors typically are in the range of 1280px, 1600px, 1920px or larger. The actual width of the browser on a desktop/laptop device will vary according to the user's preference at the moment, since the browser window is resizable, but the difference between a small phone and desktop/laptop browser viewport is still huge.

## The Device's Actual Pixel Width

Many devices these days have extra-high-resolution screens, such as Apple's Retina screens. Retina screens have double the pixel density as regular screens within the same dimensions. 

Retina screens have twice as many pixels in the width, and twice as many pixels in the height, which results in a total of 4 Retina pixels for every 1 regular pixel. Retina devices interpolate the values within those 4 pixels.

An iPhone 6 Plus, for example, has an actual pixel width of 828, but because of the interpolation, web designers can treat it as a device with a width of 414 pixels.

## The Interpolated CSS Pixel Width

If high-resolution screens displayed web pages at their actual size, according to physical pixel measurements, the web pages would look half the size that they should. Nobody would like that, so high-resolution devices interpolate the value to make web pages look normal. The interpolation works well, especially for fonts and vector graphics.

### Images on High-Resolution Screens

The interpolation also works with raster graphics (PNG, JPG, GIF), but high-resolution screens expose the low resolution of the original images, making them look more jagged or blurrier. The double pixel density means that raster graphics on Retina devices look best when they are designed at twice the resolution of graphics for regular monitors, then resized by the web page to their intended dimensions.

As expected, doubling the resolution of images impacts page load time, but it also improves the visual appearance, and can be especially beneficial for users with low vision when they zoom in on the images.

## The Default Shrink-to-Fit Display Width

To accommodate the wide designs of web sites designed for desktop/laptop screens, mobile devices set a default display width, which is 980 pixels on the iPhone. This means that if the web developer does not specify any device-specific viewport settings, the iPhone will render the design at 980 pixels wide, then shrink the design to fit within the screen's viewport.

In most cases, the layout of the resulting page looks as it would on a desktop/laptop, which is nice, but after the shrink-to-fit feature has been applied, the design is too small for most users to read, forcing them to zoom in on the page. 

After zooming, the users may need to swipe or scroll horizontally as well as vertically. The zoomed page isn't optimized for the device dimensions, but at least it is readable.

## Portrait versus Landscape Width

To make things even more complicated, the device could be held vertically in portrait mode or horizontally in landscape mode, changing the dimensions in a different way.

## So Many Widths to Keep Track of!

Yes, there are a lot of widths to keep track of on mobile devices. There is the actual pixel width of the device, the interpolated CSS pixel width, and the default display width, and each of these changes depending on whether you hold the device in portrait or landscape orientation.

The good news is that for responsive CSS design calculations, we can mostly ignore the device's actual pixel width and default display width, allowing us to concentrate just on the interpolated CSS width. One of the tricks to make this happen is to specify the viewport with the meta viewport tag, discussed in the "Allowing Mobile Zoom" section of this course.