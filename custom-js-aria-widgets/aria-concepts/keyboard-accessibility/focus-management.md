# Focus Management

## Ensure the programmatic focus order matches the visual focus order.

In strict terms, the focus order is the focus order - "focus" is a term describing a behavior a document object can have. However, because focus typically follows the order in which the objects appear in document source, it may not match the order which users expect to interact with the objects on the page.

This typically happens because of one or more of the following factors: The "order" of the elements is wrong. In other words, elements have been positioned on page via CSS in a way that alters their visual location, taking things out of where they normally would be and placing them earlier (or later) than they otherwise would be based on their source position.

Or, elements are "hidden" visually, scripted to appear based on an event of some kind, but have not been taken out of the tab order. This means they're focusable even if focus is not rendered visually. Or, the interaction expected from users follows a path which doesn't match the placement of items in the document source.

## Render dynamic content inline with the controls that invoked the content.

The addition or modification of content on the page via scripting often occurs as the result of an action by a user. For instance, a new layer may appear to introduce a form after a user clicks a 'log in' link.

In practice, the `<div>` that holds the form may be at the bottom of the page, before the closing `<body>` tag, and hidden using CSS. Activating the "log in" link may show the login form visibly, but it still will exist very late in the actual tab order. To overcome this, there are two possible approaches for accessibility:

One option would be to insert the login form into the page via AJAX as the very next item in the document source. Another option would be to shift focus to the login form when it is opened, which makes it function as though it were the next item in the document source.

Regardless of the approach used to implement it, the end result must be that the next thing that gains focus is the next logical thing with which the user will interact.

## Avoid device-dependent events.

Device-dependent events are those events which require the user to have any specific input device, such as a mouse.

It is possible for developers to provide event bindings which do not require the use of a specific device or which combine events so that one type of hardware is not required. For instance, instead of using events to respond to mouse movements such as mouseover or hover, the developer can use onfocus or blur.

Doing so would enable the interface to respond to the user's actions regardless of whether or not they use the mouse.

## Ensure all actionable elements can receive focus. Avoid applying events to elements which are typically not able to receive focus unless focus will be managed.

As mentioned earlier, only certain elements are able to receive focus natively within the browser. Applying events to elements not natively focusable will often mean they are not accessible to keyboard users unless the events chosen react to the appropriate keystrokes and the actionable element has been placed in the tab order.

The shortest path to success with this requirement is to ensure events are bound to natively-focusable elements, for instance `<a>`, `<button>` and `<input>`. Binding events to other elements - such as a `<td>` for table sorting - carries the extra requirement to add the item to the tab order via the tabindex attribute. Doing so is a simple but highly effective step to improve accessibility.

## Ensure that simulated controls, simulated dialogs, calendar controls, embedded media content, menus and other actionable dynamic content can be accessed, operated, and closed from the keyboard.

When it comes to keyboard accessibility and focus control, users must be able interact with the system without being required to use a mouse. This is because they may be either unable to see the mouse pointer or may lack the fine motor control necessary to use a mouse effectively.

Interfaces which rely on client-side scripting are typically no longer a problem for users with disabilities, provided that the interactivity from such an interface can be performed using the keyboard. Controls and user interface elements not made from standard HTML may pose challenges for keyboard access.

Things such as simulated dialogues, simulated calendar controls, drag-and-drop interfaces, light boxes and so on must be accessible via the keyboard; and users must be able to open them, operate them, and close them using a keyboard only.

## Ensure that focus shifts back to the point where interaction started when the simulated dialog or control is closed.

One of the biggest challenges when creating rich web interfaces using JavaScript is the management of focus when new content or controls are added or removed from the page.

Whenever new content appears on the page as a result of the user invoking a control, the interaction flow must be circular so that the user returns to the place from which the interaction first started. Typically, this circular flow is implicit, meaning that users without disabilities naturally continue where they left off.

From an accessibility point of view, users with disabilities expect the same interaction and consequently focus must be shifted back to the point where their interaction started.

## Ensure that focus changes appropriately when dynamic content changes.

The presentation or modification of content on the screen may require that the user interact with — or at the very least, take notice of — the new or changed content. It is important to have a clear indication of page content that has been updated.

This allows the user to understand the change and also allows a keyboard user to interact with any new content. How this happens often depends on the type and nature of the content. For example:

- For content added to the screen in reaction to a user-fired event, focus should be shifted to the new content
- For content removed from the screen in reaction to a user-fired event, focus should be shifted to the next logical place in the interaction
- For content changed that is not in reaction to any user-fired event, the user should be notified of the change

## Avoid opening new windows without user notice; Avoid opening new windows based on focus change.

Opening new windows in general is a bad idea and one that most people would advise avoiding. For accessibility, new windows can be confusing to AT users because they cause an unexpected browser action.

They can be especially problematic to users of screen enlargers, or even users that have their monitor set to a larger resolution, as new windows can appear outside of the viewport, requiring the user to scroll the viewing area to hunt for the new window.

Primarily the issue can be mitigated as long as the user is aware that a new window has been opened, so that they can close it and go back to the parent window, if necessary. Consequently, users should be given notice — in the body of the link — that a new window will be opened.

When the user encounters the link, the notification will alert them of the new window. Opening a new window based on a focus change (such as a user hovering over a link) is ill-advised, even if the notification exists. This is because the focus event will be triggered — and the new window will open — before the notification is actually rendered to the user.

Therefore, any opening of new windows should occur as a direct result from a keypress or click event.

## Provide keyboard interactions to simulated controls which mimic their desktop equivalents.

When creating interface elements intended to mimic the appearance and operation of standard desktop controls, for instance, tree menus, alert boxes, dialogs, and so on, provide keystroke combinations which allow the controls to be operated in the same way as their desktop-based inspirations.