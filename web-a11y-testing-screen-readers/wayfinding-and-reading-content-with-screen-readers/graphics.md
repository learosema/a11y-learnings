# Graphics

## How screen readers treat images

### Alt text

Screen readers read the alt attribute of images if alt text is provided and will announce the word "graphic" before the alt text. For example,
`<img src="cat_0123.jpg" alt="A tabby cat playing with a ball of string">`
will be read as "Graphic, a tabby cat playing with a ball of string."

Note: Don't say "image of..." or "graphic" (or similar) in the alt text, because screen readers already say that!

### Missing alt text

If an image does not have alt text, JAWS announces the image's file name. For example, `<img src="cat_0123.jpg">`

### Null alt text

Screen readers completely ignore images marked with null (empty) alt text (which is what you want them to do, if you've used null alt text on purpose). For example, screen readers will say nothing when they come across `<img src="cat.jpg" alt="">`.

### Linked images

If an image is a link, JAWS says "link graphic" before saying the image's alt text. For example,
`<a href="cat_page.html"><img src="cat_0123.jpg" alt="A tabby cat playing with a ball of string"></a>`
will be read as "Link graphic, a tabby cat playing with a ball of string."

### Linked images missing alt text

If the image without alt text is a link, JAWS will generally read the link destination, which is the href attribute in the HTML markup for the link. For example,
`<a href="cat_page.html"><img src="cat_0123.jpg" alt=""></a>`
will be read as "Link graphic, cat underscore page dot H T M L"

### Image map hot spots

JAWS reads the alt text for image map hot spots; therefore, the alt text should describe the link destination.

## Method 1: List all graphics

- JAWS with Chrome, Edge, Firefox, IE: Insert + Control + G
- NVDA with Firefox, Chrome, Edge: Not available
- VoiceOver with Safari (iOS): Not available
- Talkback with Chrome, Firefox: Not available
- VoiceOver with Safari (macOS): Control + Option + U (to open rotor), then use left/right arrows to select Images
- Narrator with Edge: Not available

## Method 2: Navigate from one graphic to the next

- JAWS with Chrome, Edge, Firefox, IE: G
- NVDA with Firefox, Chrome, Edge: G
- VoiceOver with Safari (iOS): Rotate two fingers on the screen (like turning a dial) to open the rotor, locate Images, then swipe right
- Talkback with Chrome, Firefox: Not available
- VoiceOver with Safari (macOS): Control + Option + Command + G
- Narrator with Edge: Not available
