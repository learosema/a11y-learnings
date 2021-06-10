# Content MUST NOT require scrolling in two directions (both vertically and horizontally) — even when the viewport is set or zoomed to 320 CSS pixels wide (for vertically-scrolling content) or 256 CSS pixels high (for horizontally-scrolling content) — unless both scrolling directions are essential to the usage or meaning of the content.

Note: 320 CSS pixels is equivalent to a starting viewport width of 1280 CSS pixels wide at 400% zoom. For web content which is designed to scroll horizontally (e.g. with vertical text), the 256 CSS pixels is equivalent to a starting viewport height of 1024px at 400% zoom.

Having to scroll in two dimensions to view content on a page makes seeing and reading the content difficult. If a user has to scroll in order to see a full line of text, it becomes very difficult to then follow to the next line. Pages must reflow as zoom increases up to 400% so that content continues to be presented in only one column. 

This is often done through responsive design that uses CSS media queries to reflow the page for different viewport sizes. Some images can be resized so that they stay within the viewport as the user increases zoom, while others need to be enlarged so that the user can see the details. 

See the [WCAG Understanding Document for this criterion](https://www.w3.org/WAI/WCAG21/Understanding/reflow) for more details.

There are exceptions to this rule. Some web page functionality requires scrolling in two directions. This can include large graphics, images or data tables where reflow is not feasible without losing meaning. 

It also includes toolbars that need to fit many buttons, which may scroll in the direction of the text.