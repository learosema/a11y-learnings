# Animated SVG Content

## SVG animations SHOULD use JavaScript, rather than the <animate> element.

There are various ways to accomplish animation in SVG, depending on the complexity of the image itself, as well as the desired animation effect(s). The acceptable methods are either declarative, using Synchronized Multimedia Integration Language (SMIL) or Cascading Style Sheets (CSS), or through JavaScript DOM manipulation. Animation could be as simplistic as changing styles or color, or more complex with geometry changes, transformations or showing and hiding various sections of the SVG document.

SMIL can be used to create both simplistic and relatively complex animations of SVGs without the use of CSS or JavaScript, but with one major downfall. Internet Explorer does not offer support for SMIL. The silver lining, if you want to look at it in that manner, is that although Internet Explorer will not render the animation, it will still render the final state of the image. As long as the other methods of creating the SVG in an accessible manner are followed, this should not be an issue from an accessibility standpoint.

Consider the following SVG example which creates an image of a simple 200 x 200 px, solid blue square. An animation effect has been added in a Declarative fashion by embedding the <animate> element within the <svg> document.

### Note

SMIL animations have been removed from the SVG 2 specifications but will still work in SVG 1.1 user agents. A new approach to element-based animations has been undertaken. For further information regarding the current state of SVG animation, please refer to the SVG/Animation opens in a new window section on the W3C Wiki.

## SVG animations MUST not flash or blink at a rate of 3 times per second or more.

Flashing or blinking content runs the risk of causing a seizure in some individuals.

## SVG animations MUST NOT auto-play for more than 5 seconds.

It is best if the animation does not play at all until the user activates the animation. As a compromise, the WCAG 2.1 guidelines allow the animation to auto-play for up to 5 seconds.

## SVG animations MUST allow users to pause the animation.

An animation that cannot be paused can be immensely distracting, especially for people with attention deficit disorder, or some kinds of cognitive disabilities.

## SVG animations SHOULD NOT distract the user from the main purpose of the web content.

Remember that just because you can technically do something, it doesn't necessarily mean you should. Generally speaking, the animation should serve a specific purpose, rather than simply adding movement to a static page.
