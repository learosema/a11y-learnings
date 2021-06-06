# Informative images

## Images that convey content MUST have programmatically determinable alternative text.

Screen readers cannot easily read or interpret images directly. They can only read the alternative text provided by the author. In order to provide a programmatically determinable text alternative for an image, authors must use the alt attribute on the img element.


### Example

```html
<img src="sewing_machine_singer.jpg" width="686" height="518" alt="A Singer model antique sewing machine">
```

## The alternative text for informative images MUST be meaningful (accurately conveying the purpose of the image, and the author's intent in a way that is useful to those who cannot see the image).

The purpose of alt text is to provide a description of the image for blind people. The alt text must provide an appropriate substitute for not being able to see the image. 

The alternative text should clearly represent the purpose of the image so that the user understands — as easily as possible — why the image is there and what it represents. 

This module will discuss specific approaches to alternative text based on how an image is used, but keep this fact in mind whenever creating alternative text: alternative text should be used to clearly communicate the intent, purpose, and meaning of the image in a way that serves as a true alternative for the image.

In deciding what to include in the alternative, it is often a good idea to consider the following questions:

- Why is this non-text content here?
- What information is it presenting?
- What purpose does it fulfill?
- If I could not use the non-text content, what words would I use to convey the same information or function?

### Good Example: Informative Image with Meaningful General-Purpose Alt Text

```html
<img src="sunset.jpg" width="700" height="466" alt="The sun setting over the Pacific Ocean,
with a silhouette of a flying seagull in the foreground">
```

### Good Example: Alternative Text for a Specialized Purpose of an Image

```html
<img src="sunset.jpg" width="700" height="466" 
   alt="The camera was set to properly expose the sunset in this beach scene,
   resulting in underexposure of the land and flying seagull in the foreground,
   turning them black">
```

### Good Example: Logo

The alt text describes the purpose of the image — which is to identify the brand — rather than its appearance.

```html
<img src="dequeUniversityShield.png" alt="Deque University" width="245" height="158">
```

Under some circumstances, it may be appropriate to identify this image as a logo. The alt text could say `alt="Deque University logo"`, for example. Usually, though, it is enough to identify the brand. It depends on the author's intended message.



