# SVG as an Alternative to Icon Fonts

## SVG icon examples

SVG icons can be monochrome (like icon fonts) or multi-colored. The collection of social media icons below includes some monochrome (Facebook, Pinterest, Twitter, WordPress, and YouTube) and some multi-colored icons (all the others).

## Advantages and Disadvantages of Icon Fonts versus SVG

There isn't a clear case to be made, from an accessibility perspective, for either icon fonts or SVG. Neither is inherently superior to the other (assuming they are implemented in accordance with accessibility best practices in each case). They both have accessibility strengths and weaknesses.

|Benefit | Icon Fonts | SVG
|---|---|---
|Icons are vector-based, rendering clearly and legibly when magnified | Yes | Yes
|Users can customize colors with accessibility utilities like Windows High Contrast Mode | Yes | No
|Icons scale with the text when magnifying only the text | Yes |No
|Icons work when images are turned off | Yes | No
|Icons can be multiple colors | No | Yes
|Icons retain their original color(s) when font and background colors are changed in user preferences | No | Yes |
|Icons work when styles are turned off | No | Yes
|Icons work when users customize the font (e.g. users with dyslexia may choose a dyslexia-friendly font) | No | Yes

### Note: Techniques matter!

The above table is accurate only if accessibility best practices are followed. When icon fonts are implemented poorly, or when SVG images don't have alternative text, they can both be bad for accessibility.

## References

- https://www.filamentgroup.com/lab/bulletproof_icon_fonts.html
- https://cloudfour.com/thinks/seriously-dont-use-icon-fonts/
- https://benfrain.com/seriously-use-icon-fonts/
- http://ianfeather.co.uk/ten-reasons-we-switched-from-an-icon-font-to-svg/
- http://fontawesome.io/accessibility/
