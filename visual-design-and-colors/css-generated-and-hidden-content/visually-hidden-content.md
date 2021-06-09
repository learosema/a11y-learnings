# Visually hidden content

## Visually hidden and inactive content MUST be hidden from screen reader users until that content is made visible and active for sighted users.

Any content or interface elements that are intentionally hidden from users — such as inactive dialogs, collapsed menus, etc. — must also be hidden from screen reader users. Once those items are made available to sighted users — such as when they activate a button or expand a menu item — the items must be made available to screen reader users. 

The goal is to give screen reader users an equivalent user experience to sighted users. If there is a compelling reason to hide content from sighted users, there is usually a compelling reason to also hide that content from blind users. And when the content is made available to sighted users, it makes sense to make it available to blind users as well.

Content will be hidden from screen reader users (and all sighted users too) when display:none or visibility:hidden are used. Changing those values to display:block, display:inline, or other display or visibility options will make the items available to screen reader users.

## When additional content is triggered on pointer hover or on keyboard focus, that additional content MUST be dismissible, hoverable, and persistent.

The purpose of this rule is to ensure that pop-up content does not prevent user access to other page content, and that users have adequate access to pop-up content. It specifically pertains to content that appears when you mouse over or bring keyboard focus to an object, like custom tooltips or submenus in a navigation bar. 

It does not apply to modal dialogs or content that is controlled by the user agent (web browser), such as built-in tooltips. It also does not apply to "Skip to main content" links that become visible when they receive focus, because there is not new content becoming available aside from the object that received focus.

Users need to be able to dismiss the new content without moving the mouse or keyboard focus when the popup obscures page content, such as a submenu that drops down over the page. This can be done through dismissing the content with the Escape key.

Users also need to be able to hover their mouse pointer over the new content. This is important for users who magnify their screen and need to be able to pan over the pop-up content, as well as users who have content read to them as they mouse over it.

Finally, content should not disappear until keyboard or mouse hover leaves it. Users need adequate time to read and process the content.

- Bad example: hover menu without possibility to close it via Escape key
- Good example: deque university nav menu with full mouse/touch and keyboard support.
