# Focus or tab order

## The navigation order of focusable elements MUST be logical and intuitive.

When keyboard users tab through the focusable items (buttons, links, form elements, custom controls, etc.), the order needs to make sense, so they don't get confused.

If a keyboard user—whether sighted or blind—uses the tab key to go through all of the focusable elements (links, buttons, form elements, etc.), the browser will start with the focusable elements at the top and proceed linearly through all the focusable elements until reaching the bottom. 

The browser ignores all of the visual formatting—columns, floating elements, margin, padding, positioning, etc.—and pays attention to the underlying order that things appear in the DOM.

## tabindex of positive values SHOULD NOT be used.

It is possible to customize the tab order of focusable items using tabindex, by setting it to numerical values like 1, 2, 3, etc., but this has the potential to cause significant problems for keyboard users.

- It causes a discrepancy between the tab order and the reading order, leading to confusion when interacting with the page using a keyboard
- It removes the items from their natural tab order, and instead places them first in the tab order. Anything with any tabindex value of 1 or greater will come before all other focusable items. For example, if only one item on the page has a tabindex set, and it's set to 9000, that item will be the first thing a user tabs to, even though the number is very large. When tabbing away from the item with tabindex="9000", the focus will next go to the first focusable item in the DOM. If the user continues tabbing through the web page, the user will eventually arrive at the place where the tabindex="9000" item is and will expect to be able to tab to it, but will not be able to, because the item's position in the DOM does not correspond to the item's tab order. The user would have already tabbed to it previously, so the browser skips over that item. It's confusing to the user—especially sighted keyboard users—when this happens.

