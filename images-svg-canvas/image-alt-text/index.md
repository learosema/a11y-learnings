# Image `alt` text

## Introduction

## Alternative Text Best Practices

This section discusses how to address accessibility in various types of images, including informative images, decorative images, complex images, and animations. Good alternative text is:

- Programmatically Determinable (screen readers can access the alternative text)
- Meaningful (the alternative text accurately describes the image's purpose or author's intent in using the image).
- Concise (the alternative text does not exceed about 150 characters, and preferably is much shorter than that)

If the image is purely decorative or redundant, it's best to use a technique to hide the image from screen readers (e.g., use `alt=""`). It is important to note that the `alt=""` technique only works in HTML content and cannot be used in Office files, such as Word documents or PowerPoint slides. In those programs, there is not currently a way to identify an image as purely decorative, so all images/graphics require an alternative text description.

If the image conveys a lot of important information, a supplementary long description will need to be included along with the image.

The overall goal is to give people who are blind an equivalent experience to those who are sighted, or at least get as close as possible without overwhelming them with long text descriptions.

## The "Accessible Name Calculation" for the `<img>` Element

There are multiple ways of adding alternative text to images. The standard (preferred) way in most cases is the alt attribute, but there are other options.

- aria-labelledby — If there is an aria-labelledby attribute, the text it refers to will override all other values.
- aria-label — The aria-label text will override all other values (if aria-labelledby is not specified).
- alt — This is the standard method of providing alternative text (note that the alt text won't be read at all if either an aria-labelledby attribute or an aria-label attribute is present).
- title — Screen readers will read the title attribute text if no other method is present. Some screen readers (e.g. VoiceOver on macOS) treat the title attribute as an additional description for the image and will read both the accessible name AND the title. Others (e.g. NVDA, JAWS) will not read the title if an accessible name is available through other methods. All screen readers read the title text if no other alternative text is provided.

Refer to the [technical explanation of the accessible name calculation](https://www.w3.org/TR/accname-aam-1.1/#mapping_additional_nd_te) for more details.

## In this Section:

- Informative Images
- Decorative or Redundant Images
- Actionable Images (Links, Buttons, Controls)
- Form Inputs type="image"
- Animated Images
- Complex Images
- Images of Text
- CSS Background Images
- Image Maps
