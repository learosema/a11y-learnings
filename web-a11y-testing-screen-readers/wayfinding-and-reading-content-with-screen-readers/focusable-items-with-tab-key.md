# Navigating Through Focusable Items with the Tab Key

## Focusable Items

One of the fastest ways to get around to the actionable elements on a page is to use the Tab key, or use Shift + Tab to go backwards. Actionable elements include:

- Links
- Form elements
- ARIA components
- Anything with tabindex="0"

As you tab around, you will hear the screen reader read the text for each link, as well as the labels for form elements, the labels for focusable ARIA controls, and the text of anything with tabindex="0". Pay attention to make sure that the link text and labels make sense when read out of context like this. Links or labels that say "more" or "read more" or "click here" do not make sense out of context.

### Note:

It's important to note that if you only tab through content, you will skip over all of the non-focusable content. Screen reader users use different methods to read through the rest of the content (e.g. the down arrow key when using JAWS or NVDA).

## The Tab key on mobile devices

On mobile devices, there isn't an exact equivalent of navigating by the Tab key, unless you connect to an external keyboard. The closest equivalent to navigating by the Tab key in iOS in touch mode would be to navigate by links or to navigate by form controls.

To navigate by links in iOS with VoiceOver, activate the rotor by putting two fingers on the touch screen and rotating them until "Links" is selected, then swipe down on the screen to go to the next link or swipe up on the screen to go to the previous link.

To navigate by form controls in iOS with VoiceOver, activate the rotor by putting two fingers on the touch screen and rotating them until "Form Controls" is selected, then swipe down on the screen to go to the next form control or swipe up on the screen to go to the previous form control.

To navigate on a mobile device to ARIA components and other focusable items that aren't links or form controls, you will need to navigate through all elements (not just the focusable ones) by swiping right to go to the next element or swiping left to go to the previous element. This is less efficient than using the Tab key on a full-size device—because you can't skip past paragraphs, divs, spans, etc.—but will work.
