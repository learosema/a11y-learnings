# Designate Links Correctly

## Links MUST be semantically designated as such.

Links need to be semantically designated as links in the markup. In other words, they need to be inside an <a> element, and they need a valid href value.

## ARIA role="link" can be used to provide link semantics

If absolutely necessary (which is almost never the case), a <span> element can work as a valid link — even for screen reader users — if the following conditions are met:

- Add `role="link"` so that screen readers recognize it as a link.
- Add `tabindex="0"` to make it focusable with the keyboard.
- Ensure that the JavaScript allows both the mouse click AND the enter key to activate the link.

## Links and buttons SHOULD be designated semantically according to their functions.

Here are the main distinguishing factors between links and buttons:

1. Links take users to different locations (either to a different page or to a different location on the same page)
2. Buttons activate scripted functionality (e.g. make a dialog appear, expand a collapsed menu, turn font bold, etc.), usually on the same page, but a button can also submit form data.
Sometimes there is a grey area, where it might be difficult to determine whether a control should be a link or a button, but in most cases the difference is clear.

## Screen reader users are informed whether something is a button or a link

Screen readers always say "link" before links, and "button" before buttons, so screen reader users always know which is which, at least in terms of the markup. 

Web developers sometimes treat the distinction lightly, sometimes giving links button-like scripted functionality, and sometimes making buttons take users to destinations as links normally would. 

The problem with this loose approach is that when a screen reader user wants to find a link, the user may pull up the list of links and not find the link anywhere because it turns out that it has actually been designated as a button in the markup, or vice versa. This kind of button and link confusion can be frustrating for screen reader users.
