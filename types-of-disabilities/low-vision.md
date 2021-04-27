# Low vision

Users with low vision can see, but their vision isn't perfect even with corrective lenses. They can't see well enough to drive or read most text unless they enlarge it.

It's not a single condition but a broad category including many different conditions.

## Possible types and characteristics

- Blur
- Blur with low contrast
- Cataracts (cloudy lense)
- Diabetic Retinopathy (complication of diabetes, damaging the retina)
- Glaucoma (umbrella term for eye conditions which damage the optic nerve)
- Hemianopia (is a loss of vision or blindness in half the visual field)
- Macular Degeneration (often age-related macular degeneration causing blurriness and reduced central vision)
- Retinal Detachment (blurred vision, flashes of light, curtain like shadow)

## Web a11y for low vision

### Screen magnification

Reading small text is extremely difficult for users with low vision. Users may need screen magnification software like ZoomText or MAGic.

- [Introduction to ZoomText and Screen Magnifiers](https://www.youtube.com/watch?v=ojtiVj78QPw)

#### Issues when using screen magnification

- when looking at large images, users using screen magnification need to move around a lot
- An alert box may appear outside the visual field of the user

### Screen readers

- people with low vision can benefit from screen readers, too
- ZoomText and MAGic have basic screen readers built-in, not as full-featured as stand-alone screen readers, but adequate

### Color Customization

- For people with low contrast/color vision, colors may not be easily visible
- text that is too close in color or luminance to the background can be hard to read
- some people experience pain when looking at bright lights
- all-white backgrounds can be difficult
- Users may modify the colors either in their operating system or in the web browser

## Design considerations for people with low vision

- Do not disable pinch to zoom (avoid `<meta name="viewport" content="user-scalable=no">`)
- all text must pass contrast guidelines (verify via aXe)
- Links, buttons and controls must have a visible `:focus` state and should have a visible `:hover` state
- User interface should provide a clear distinction between content and controls

## More

- https://www.zoomtext.com/
- [Leanne Cough illustrates the benefits of ZoomText](https://vimeo.com/13757711)
