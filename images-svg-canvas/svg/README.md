# SVG

## Introduction

Scalable Vector Graphics (SVG) provide a number of features that aid in the accessibility of graphics on the web. They provide particular benefit for individuals who are blind or with low vision who may utilize assistive technologies, or others who experience color blindness. The added benefit of the accessibility features of SVG is that they can also increase the usability of content for those without disabilities, such as those who utilize mobile devices or other non-traditional (e.g., tablet) devices for accessing the web.

This section will limit its focus to the accessibility features of SVG. It is not intended to provide details of the various options for creating and implementing Scalable Vector Graphics. A very comprehensive resource, [A Compendium of SVG Information](https://css-tricks.com/mega-list-svg-information/), can provide details on everything from basic implementation to gradients, animations and all kinds of other goodies.

## What are Scalable Vector Graphics?

SVG are two-dimensional, vector-based graphics defined in XML format. They can be created and edited with a text editor but are more likely created with graphic editing software such as Adobe Illustrator or Inkscape. SVG is actually a language itself, similar to HTML, and was first introduced by the W3C in 1999. Unfortunately, up to this point in time SVG has not been widely utilized for graphic development, due to lack of browser support. Today, however, it has support from most modern browsers, though some variances in the way they are interpreted by different types of screen readers can occur. Additionally, it should be noted that support for animation does not exist in Internet Explorer.

Three types of graphical objects can be created using SVG including vector shapes, such as paths with straight lines or curves. Additionally, images and text can also be created. SVG can also be interactive and dynamic, triggered either declaratively by embedding the animation inline, or alternatively via scripting.

SVG objects are resolution independent, meaning they will look as good on a small, mobile device as they will on a desktop PC with a 24-inch monitor. This is significant for users with low vision and those who utilize some assistive technologies that may have a very low resolution. Furthermore, because the image is created using mathematical principles it will scale seamlessly, whether it is expanded or shrunken, meaning SVG is an optimal solution for responsive design.

## In this Section

- [Raster versus Vector Graphics](raster-versus-vector-graphics.md)
- [SVG as img src](svg-as-img-src.md)
- [Inline SVGs](inline-svgs.md)
- [Embedded SVGs](embedded-svgs.md)
- [Complex Alternative Text](complex-alternative)
- [Text in SVGs](text-in-svgs.md)
- [SVG Color Contrast](svg-color-contrast.md)
- [Animated SVG Content](animated-svg-content.md)
- [Interactive SVGs](interactive-svgs.md)
