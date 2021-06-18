# Changes in Context

## Overview

It can be confusing and disorienting to users if a user action automatically triggers a change of context that the user is not expecting. A change of context is defined as a change to:

- The user agent (e.g. when links or buttons that cause the user to leave the web browser and automatically open a different application).
- The viewport (e.g. when the screen scrolls down or up, or when elements visually replace, obscure, or alter the position of the elements previously in view, or when a new window opens)
- The focus (e.g. when the keyboard focus is forced to another element)
- The content (e.g. when the meaning of the page changes significantly, or when elements on the page are rearranged)

None of these kinds of scripted actions are inherently bad in concept. The danger to accessibility is when they happen automatically, without the user explicitly requesting the actions. 

Users should be allowed to press a button or perform some other similar kind of action to request a change of context, rather than have the web page assume the user wants to change the context based on actions that are, from a user experience perspective, more ambiguous, like hovering the mouse over an element, or focusing on an element with a keyboard, or changing the value of a form input.

Under most circumstances, it would be wrong to assume that the user has finished making a choice based on any of those kinds of interactions.

## Focusing on an element MUST NOT automatically trigger a change of context, unless the user has been adequately advised ahead of time.

Attaching a scripted behavior to a focus event can be disorienting for users of all kinds, and particularly for screen reader users, who may have a hard time figuring out what happened. Keyboard users in general need to be given the freedom to navigate forms without having events triggered simply by focusing on a form field.

- [Bad example: dialog triggered by focus](https://dequeuniversity.com/assets/html/module-forms/context/bad/focus/index.html)

## Changing an element's value MUST NOT automatically trigger a change of context, unless the user is adequately advised ahead of time.

Note: Changes to the context are allowed as a result of activating a "submit" button (or similar), because the assumption in that case is that the user is finished exploring, inputting, or selecting options, and is ready to proceed.

- [Bad: navigation triggered by change event in select field](https://dequeuniversity.com/assets/html/module-forms/context/bad/change/index.html)

## Hovering over an element with the mouse MUST NOT automatically trigger a change of context, unless the user has been adequately advised ahead of time.

Triggering a change of context as the result of a mouse hover action is a rather drastic way to respond to user mouse movements. It is highly unexpected and confusing for users.

- [Bad: dialog triggered by hover](https://dequeuniversity.com/assets/html/module-forms/context/bad/hover/index.html)