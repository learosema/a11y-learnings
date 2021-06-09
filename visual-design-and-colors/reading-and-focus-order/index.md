# Reading Order, Focus Order

## Introduction:

The DOM order determines the reading order and tab/focus order. When screen reader users navigate straight through the content linearly, the order that they hear the content is determined by the order in the document object model (DOM), which is essentially the source code after the browser has parsed it and run any relevant JavaScript. 

This seems intuitive enough, but here are some things to watch out for:

CSS positioning techniques — such as float:left, float:right, position:absolute, position:relative, position:fixed, margin, padding, etc. — can alter the visual layout in ways that don't match the reading order in the DOM.

Injecting content dynamically via JavaScript or AJAX can place things in an unexpected location, such as above the user's current focus. A blind person may not realize that new content has been added to the document, especially if the user has already visited that area of the page. 

There is no obvious reason for the blind person to navigate backward just to find out if maybe something has been added or altered in an area they've already been to.

### Note

Screen reader users can navigate around a page in many ways in addition to the tab order. For example, they can navigate by headings, landmarks, tables, graphics, lists, links, and other elements. Even so, the DOM still determines the order of these elements, which is why it is so important to get the DOM order right.
