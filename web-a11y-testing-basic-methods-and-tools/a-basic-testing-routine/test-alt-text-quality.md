# Test Alt Text Quality

## Overview

Text alternatives for images should be functional and provide an equivalent experience for users who are unable to see the images. Depending on the context in which the image is used, it may not always be necessary for the image itself to be described, but rather its function may be described.

For instance, if a magnifying glass icon is used to identify a search button, the alt text for the icon wouldn't be "magnifying glass", but "Search". Alternative text should also be brief and concise, usually no longer than 150 characters.

When alternative text exceeds this length, it may be too long and verbose for assistive technology users. Alternative text does not function like actual text, so users cannot repeat statements within the text alternative, but would have to read or listen to the alternative text all over again. There are some exceptions to this best practice, but shorter alt text is generally the accepted practice.

Every `<img>` tag should have an alt attribute. Automated testing can determine whether the alt attribute is missing; but manual testing is needed to determine whether text alternatives provided for images convey the information that is useful for understanding and interacting with web page content. Manual testing is also required to ensure background images — those provided via CSS rather than an `<img>` tag — have alternative text provided at all and determine if it is useful.

There are a number of different types of images that can be present on a web page, and the alternative text needs to be evaluated in context to determine if it is appropriate for every image.

## Common Types of Images

There are several different types of images that can be used on a web page and there are general approaches to how alternative text should be composed and provided for these types of images. The table below identifies these common types of images and provides guidance on alternative text methods. However, when testing for the quality of text alternatives, it is key to view the image and judge how the image is used in context on the web page. To learn more about images and accessibility, go through the course, Images, SVG, and Canvas.

## Alternative text considerations for various types of images

### Active (or Actionable)

- Alternative text should describe the functionality of the image or the destination if the image is used as a link.

### Informative and Informative Background (CSS)

- Alternative text should describe the purpose of the image, convey information in the image that allows users to understand how it contributes to web page content.

### Decorative

If the image is purely decorative, there should be no text alternative. Keep in mind, if the image is provided using an <img> tag it still needs an alt attribute, but the value should be empty (or null) so assistive technologies will ignore the image (in code, it looks like alt="").

### Redundant

If an image is right next to actual text that describes the image, alternative text should not be provided. It will just repeat the description that is provided in the text next to it. Again, if the image is provided using an <img> tag it still needs an alt attribute, but the value should be empty (or null).

### Complex (e.g., Charts, Graphs)

Complex images need both alternative text and a long description. Since alternative text is supposed to be brief, an extended description needs to be provided to convey all the information presented in a complex image. The long description should be easy to locate and should be an equivalent substitute of information within the image. Presenting the information in a different format, such as a data table, is an acceptable substitute for a complex image.

### Input

Alternative text should be an accurate description of the form input, control, or button; but the alternative text should not include the role of the input, control, or button. For instance, alternative text for a Submit button should say "Submit", not "Submit button". If the alternative text includes the role, the role may be rendered twice to those using assistive technologies like a screen reader.

### Canvas

Meaningful alternative text for `<canvas>` images should be provided either through the aria-label or aria-labelledby attribute. For complex `<canvas>` images, additional description should be available through an aria-describedby ID reference to text in the DOM.

## Testing Methodology

When checking for alternative text, we are generally looking for the following:

- Alternative text exists: Every image has appropriate alternative text.
- Alternative text is descriptive: The alternative text should describe the purpose of the image in a way that adequately substitutes for the image.
- Alternative text is concise: Alternative text should be brief. There is no official limit, but a limit of approximately 150 characters is considered best practice.
- Long description exists for complex images: The long description is on the same page, near the complex image, or available in a link to another page.
- Long description is an adequate substitute for the image: Someone who cannot see the image should be able to make sense of it and understand the purpose of the image based on the long description.

Alternative text isn't visible on the web page, as it is provided through code. So, if the image is provided through an <img> element, the easiest way to evaluate alt text is to use a screen reader. A screen reader allows users to browse images on a web page by using specific keystrokes.

However, if the image is a background image that conveys information or meaning, alternative text must be provided through aria-label, aria-labelledby, or some other method like clipped or offscreen text.

Alternative text for these types of images will not be conveyed through a screen reader's keystrokes for graphics navigation if it doesn't have the ARIA role="img" assigned to it. You may have to navigate through the web page in the screen reader's traditional document mode to hear the alternative text or inspect the code to see if alternative text is provided through one of the alternative methods mentioned above.

### Desktop Web

- Open the web page using the testing screen reader and its compatible web browser (e.g., JAWS and Chrome, Firefox, or Internet Explorer).
- Use the keystroke associated with images (or graphics) to browse the images on the web page:
  For NVDA and JAWS, the keystroke is G
- When using VoiceOver, you can navigate by images or generate a list of images using the Rotor. The keystroke to use while browsing a web page is Control + Option + Command + G. To use the Rotor, type the keystroke Control + Option + U, and use the arrow keys to find the list of images on the web page.

#### Bad Example

On the MarsCommuter demo site, there are several images in the carousel/scrolling widget that have insufficient alternative text. In the screenshot below from the site, the alternative text for the image next to the "Free Astronaut Ice Cream" heading says "icecream.jpg".

### Mobile Web

#### Using Talkback and Firefox:

- You can either enable "Explore by Touch" (recommended) or use gestures to read and interact with the web page.
- If you use Explore by Touch, you can move your finger around the screen and the screen reader will render the content under your finger.
- For gestures, swipe right on the web page to read the next item on the web page.
- Once you encounter an image, determine if the alternative text is appropriate for the image.

#### Using VoiceOver iOS and Safari:

- Once you are on the web page, launch the Rotor by placing two fingers on the screen and moving them in a circular motion.
- Use up or down swipes to find the list of images on the web page.
- Use left or right swipes to select an image from the list.
- Once you select an image, determine if the alternative text is appropriate for the image.

Note: If swiping bypasses an image or explore by touch does not speak an image, it may be a CSS/background image or an icon font with no image role (role="img"). If a CSS/background image or icon font is decorative, that is fine, but if it is meaningful it needs alternative text.
