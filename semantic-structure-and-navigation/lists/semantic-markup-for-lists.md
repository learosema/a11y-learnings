# Semantic markup for lists

## Lists MUST be constructed using the appropriate semantic markup.
There are three main types of lists in HTML:

- Unordered lists (`<ul>`) render as bulleted lists of list items (`<li>`). Unordered lists should be used when a set of items can be placed in any order.
- Ordered lists (`<ol>`) render as numbered lists of list items (`<li>`). Ordered lists should be used when the list items need to be placed in a specific order.
- Definition lists (or Description lists in HTML5) (`<dl>`) render as paired terms (`<dt>`) and definitions (`<dd>`). Definition/description lists are used to pair a term with its definition or a name with a value.
Screen readers notify users when they come to a list and tell them how many items are in a list. This helps listeners know what they are listening to, and what to expect as they listen to it.

If you don't mark up a list as a real list—for example, if you use a table to create a fake list, or you use the `<br>` element to create a fake list—screen readers cannot inform the listener that they are listening to a list, and cannot let them know how many items are in the list.
