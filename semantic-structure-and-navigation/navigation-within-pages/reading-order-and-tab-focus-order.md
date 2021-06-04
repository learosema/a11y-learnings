# Reading Order and Tab/Focus Order

## The DOM order determines the reading order and tab

When screen reader users navigate straight through the content linearly, the order that they hear the content is determined by the order in the document object model (DOM), which is essentially the source code after the browser has parsed it and run any relevant JavaScript. This seems intuitive enough, but here are some things to watch out for:

- CSS positioning techniques can alter the visual layout in ways that don't match the reading order in the DOM.
- Injecting content dynamically via JavaScript or AJAX can place things in an unexpected location, such as above the user's current focus. A blind person may not realize that new content has been added to the document, especially if the user has already visited that area of the page. There is no obvious reason for the blind person to navigate backward just to find out if maybe something has been added or altered in an area they've already been to.

## The reading order MUST be logical and intuitive.

If the reading order is illogical or unintuitive, the content will not make sense, or it will be difficult to understand.

Screen readers ignore all of the CSS layout in your web design. Turning off the style sheets is one way to check the reading order of static content. When the content is stripped bare of the visual styling like this, it is sort of how a screen reader "sees" it.

## The navigation order of focusable elements MUST be logical and intuitive.

When keyboard users tab through the focusable items (buttons, links, form elements, custom controls, etc.), the order needs to make sense, so they don't get confused.

If a keyboard user—whether sighted or blind—uses the tab key to go through all of the focusable elements (links, buttons, form elements, etc.), the browser will start with the focusable elements at the top and proceed linearly through all the focusable elements until reaching the bottom. The browser ignores all of the visual formatting—columns, floating elements, margin, padding, positioning, etc.—and pays attention to the underlying order that things appear in the DOM.

## tabindex of positive values SHOULD NOT be used.

It is possible to customize the tab order of focusable items using tabindex, by setting it to numerical values like 1, 2, 3, etc., but this has the potential to cause significant problems for keyboard users.

### It causes a discrepancy between the tab order and the reading order

This is leading to confusion when interacting with the page using a keyboard

### It removes the items from their natural tab order

Instead the items are placed first in the tab order. Anything with any tabindex value of 1 or greater will come before all other focusable items. 

For example, if only one item on the page has a tabindex set, and it's set to 9000, that item will be the first thing a user tabs to, even though the number is very large. 

When tabbing away from the item with tabindex="9000", the focus will next go to the first focusable item in the DOM. If the user continues tabbing through the web page, the user will eventually arrive at the place where the tabindex="9000" item is and will expect to be able to tab to it, but will not be able to, because the item's position in the DOM does not correspond to the item's tab order. 

The user would have already tabbed to it previously, so the browser skips over that item. It's confusing to the user—especially sighted keyboard users—when this happens.
