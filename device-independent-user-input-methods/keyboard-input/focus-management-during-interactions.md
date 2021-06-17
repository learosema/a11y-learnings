# Focus Management During Interactions

## The focus MUST be purposely moved or set (via JavaScript) onto the appropriate element when the user's action requires a change of context or location for effective keyboard or touch interaction.

One of the biggest challenges when creating rich web interfaces using JavaScript is the management of focus when new content or controls are added or removed from the page. Whenever new content appears on the page as a result of the user invoking a control, the interaction flow must be circular so that the user returns to the place from which the interaction first started. Typically, this circular flow is implicit, meaning that users without disabilities naturally continue where they left off. From an accessibility point of view, users with disabilities expect the same interaction and consequently focus must be shifted back to the point where their interaction started.

The presentation or modification of content on the screen may require that the user interact with—or at the very least, take notice of—the new or changed content. It is important to have a clear indication of page content that has been updated. This allows the user to understand the change and also allows a keyboard user to interact with any new content. How this happens often depends on the type and nature of the content. For example:

For content added to the screen in reaction to a user-fired event, focus should be shifted to the new content.
For content removed from the screen in reaction to a user-fired event, focus should be shifted to the next logical place in the interaction.

[Example](https://dequeuniversity.com/assets/html/module-input-methods/dialog-focus/good1.html)

## The focus MUST NOT become lost or reset to the top of the page, except when loading or re-loading a page.

When a user activates or deactivates a feature, like a dialog, the focus must always follow the action. The focus needs to go into the activated element (e.g. into a dialog), and then after deactivating a feature, the focus must either return to the original control (e.g. the button that opened the dialog), or go to another logical location, depending on the context.

If the focus is not set to a specific location after deactivating the element currently in focus, the focus will be lost, effectively sending the focus back to the top of the DOM.

Keyboard users will find it frustrating to have to tab forward to their original position again. Screen reader users may also become disoriented, perhaps wondering if they ended up on a different page, or if the page reloaded.

[Bad example: focus is lost after closing dialog](https://dequeuniversity.com/assets/html/module-input-methods/dialog-focus/bad1.html)

## When moving or setting focus, the destination element MUST contain programmatically determinable text.

When sending the focus to a specific part of the web page using JavaScript, the container must have programmatically determinable text for the screen reader to read. Otherwise, the screen reader will be silent and users will not know that anything happened or that the focus moved at all.