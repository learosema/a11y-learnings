# Image maps

## The alternative text for the <img> of a client-side image map MUST be available as programmatically determinable text.

The alternative text for the img element for an image map must describe the image map as a whole. Using the alt attribute on the img will provide a programmatically determinable description of the image to assistive technology users.

## The alternative text for the <img> element of a client-side image map MUST be meaningful (accurately describing the purpose or author's intent in a way that is useful to people who cannot see the image).

The alternative text provided for the img element of an image map must describe the purpose of the entire image map to a user. You may even choose to provide brief instructions telling the user how to interact with the image map.

## The length of the alternative text for the <img> element of client-side image maps SHOULD be concise (no more than about 150 characters).

There is no technical limit nor policy restriction on the length of alt text, but alt text is not as usable as regular text for several reasons:

Screen reader users cannot resume where they left off if they pause while in the middle of reading alt text.
Screen reader users cannot navigate the text (e.g. by word, character, etc.).
Some older screen readers do not read the full length of the alt text.


## The alternative text for the <area> of a client-side image map MUST be available as programmatically determinable text.

Just like with the img element, alternative text must be provided for the area elements within the image map. The alt attribute on the area element will provide users with a programmatically determinable description of each portion of the image map.

## The alternative text for the actionable <area> element of a client-side image map MUST be meaningful (accurately describing the purpose or result of the action in a way that is useful to people who cannot see the image).

For area elements, the alternative text provided for each area must describe the intent, purpose, destination, or functionality of that particular section of the image map.

The length of the alternative text for the <area> element of client-side image maps SHOULD be concise (no more than about 150 characters).
There is no technical limit nor policy restriction on the length of alt text, but alt text is not as usable as regular text for several reasons:

- Screen reader users cannot resume where they left off if they pause while in the middle of reading alt text.
- Screen reader users cannot navigate the text (e.g. by word, character, etc.).
- Some older screen readers do not read the full length of the alt text.

## Server-side image maps SHOULD NOT be used when a client-side image map (or other method) can accomplish the same functionality.

## Example

```html
<img src="solar_system.jpg" alt="Solar System" width="472" height="800" usemap="#Map1">
  <map name="Map1">
    <area shape="rect" coords="115,158,276,192" 
     href="http://en.wikipedia.org/wiki/Mercury_%28planet%29" target="_blank" alt="Mercury">
    <area shape="rect" coords="115,193,276,234" 
     href="http://en.wikipedia.org/wiki/Venus" target="_blank" alt="Venus">
    <area shape="rect" coords="118,235,273,280" 
     href="http://en.wikipedia.org/wiki/Earth" target="_blank" alt="Earth">
    <area shape="rect" coords="119,280,272,323" 
     href="http://en.wikipedia.org/wiki/Mars" target="_blank" alt="Mars">
    <area shape="rect" coords="119,324,322,455" 
     href="http://en.wikipedia.org/wiki/Jupiter" target="_blank" alt="Jupiter">
    <area shape="rect" coords="118,457,352,605" 
     href="http://en.wikipedia.org/wiki/Saturn" target="_blank" alt="Saturn">
    <area shape="rect" coords="119,606,308,666" 
     href="http://en.wikipedia.org/wiki/Uranus" target="_blank" alt="Uranus">
    <area shape="rect" coords="117,664,305,732" 
     href="http://en.wikipedia.org/wiki/Neptune" target="_blank" alt="Neptune">
  </map>
```
