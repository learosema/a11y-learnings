# Image

## Don't Assume Everyone Can See Images

## Alternative Text

Provide short, meaningful alt text that serves as an effective replacement for the image for people who can't see it.

## Introduction

Let's start with the obvious: blind people can't see images.

An image, by itself, is useless to a blind person because screen readers aren't smart enough to be able to interpret the image or read the image. Screen readers can read only text. Every time you add an image to a web page, you have to add a text alternative for that image.

On the web, you do that by adding text to the alt attribute (alt stands for alternative text). This alt text is usually invisible. Most of the time, your sighted users will not see it. However, if an image doesn't load properly (for instance, if the Internet connection is too slow), the alt text will be displayed.

But usually, the only people who will know the alt text is there are your blind users, who will hear the alt text read out loud to them, or they will feel characters with their fingers if they are using braille output.

## Good Example

When a screen reader comes to an image, it says "graphic", then reads the alt text for the image. For example, when a screen reader comes across the image below, it will say:

  "Graphic, An ancient cave painting in France showing two deer with antlers, plump bodies, and small legs. One deer appears to be fallen over or dead".

The alt text is not rendered on the web page, but screen readers will read it just fine, making the image accessible to those who can't see it.

![An ancient cave painting in France showing two deer with antlers, plump bodies, and small legs. One deer appears to be fallen over or dead](cave_painting.jpg)

The image with alt text looks like this in the source code:

```html
<img src="cave_painting.jpg" alt="An ancient cave painting in France showing two deer with antlers, plump bodies, and small legs. One deer appears to be fallen over or dead" width="503" height="346">
```

## Conclusion

If you don't add alt text to an image, screen readers won't know what to say, so they will either skip over the image or try to read any related text they can find, such as the image's file name or the link destination if the image is in a link.

Sometimes file names and link destinations can be useful, but not if the text is something like `"DSC800031.jpg"` or `"index.php?v=5&token=JDNid8ahOD73do5050"`. It's much better to add good alt text than to leave it up to the screen reader to figure something out.

Writing good alt text is a bit of an art form that goes beyond the scope of this introductory course, but the basic principle is easy to remember: all images require alternative text.