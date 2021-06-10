## Linear Text Reflow

## Let the Main Content Fill the Width of the Viewport

The smaller the device, the less a person is going to be able to see on the screen, so it's usually best to fill the entire width with the main content, leaving just a little bit of padding or margin on the sides so that the text doesn't run into the sides of the screen.

## Eliminate Multiple Columns

On larger screens, multiple columns look fine. In fact, the larger the screen, the more appropriate columns become, because it's hard to read extremely wide paragraphs of text. People lose their place in wide paragraphs when they reach the end of the line and have to find the beginning of the next line. But the opposite is true on very narrow screens. If you try to cram two or more columns into a very small space, the text in those columns is hard to read because each line contains only a few words. The reading experience is choppy and hard to follow. Also, when users zoom in on one of the columns, they must pan to the side to see the other column, which is less intuitive and less friendly than scrolling down.

Formatting content in a single column may require some design sacrifices. There are fewer options simply because there is less space. That's one of the design constraints on mobile devices. You just have to accept it and let some things go. It's a different environment.

## Linearized Content Helps Screen Reader Users

Linearizing the content into a single-column design helps make things friendlier for blind users too. The screen readers the blind people use read content linearly, in the order that it appears in the DOM (Document Object Model). Sometimes on complex desktop designs the visual layout does not match the DOM reading order, which can lead to screen readers reading content in the wrong order. If your mobile design has a good linear layout, you've already done most of what you need to do to ensure a good, logical reading order for screen reader users.

## Eliminate Most Floating Objects

Floating images, with text wrapping around them, may look great on a desktop design, but they are problematic on mobile designs, unless the image is very small. It's usually best to place images and other similar objects in their own paragraph or <div> and let them appear in the same single-column flow of content.

## Eliminate Horizontal Scrolling/Panning

One of the biggest nuisances that people with low vision have to deal with is horizontal scrolling on desktop devices and horizontal panning gestures on mobile touchscreen devices. Users have to move around in every direction to find the content. It would be much easier to find things if they only had to look in the vertical direction. Good responsive designs make sure the layout actually fits within the width of the device's viewport, preferably eliminating any horizontal scrolling or gestures to pan the content into view.

## Allow Text to Reflow by Eliminating Fixed Widths and Minimum Widths

Fixed widths and minimum widths are the main cause of mobile designs that force users to scroll or pan to the side. Small devices leave little room for error when it comes to setting fixed widths, and with so many different sizes of devices, it's almost impossible to account for them all anyway. It's safer to use percentages for widths—or to not set widths at all—in mobile environments. Let the text reflow as necessary on every device to take full advantage of the available viewport.

You may still be able to use fixed or minimum widths on your desktop version, but on smaller devices, fixed or minimum widths don't work well, and they cause problems for people with low vision.