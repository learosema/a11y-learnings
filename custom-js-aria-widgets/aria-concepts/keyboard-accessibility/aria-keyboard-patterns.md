# ARIA Keyboard Patterns

## Overview

As the web has moved away from a pure document model toward a full-featured interactive application model, JavaScript programmers have sometimes struggled to come up with keyboard interaction patterns that make sense for the web.

Web interactions were typically limited to the use of the tab key and the enter key, with the arrow keys being used only rarely.

In contrast, operating systems like Windows, macOS, and Linux have had more sophisticated keyboard design patterns that take advantage of the full range of keyboard options, with extensive use of the arrow keys, as well as modifier keys like Control, Alt, Shift, Command, function keys (F1, F2, F3, etc.), and so on.

## ARIA keyboard best practices

ARIA includes keyboard interaction patterns that are more in line with the desktop model, to give JavaScript programmers more flexibility, and to give users a more consistent and efficient experience across desktop and web applications.

The [WAI Authoring Practices](http://www.w3.org/WAI/PF/aria-practices/) documentation provides recommended [keyboard interaction patterns](https://www.w3.org/TR/wai-aria-practices/#aria_ex) for many of the most common types of JavaScript widgets such as accordions, autocomplete, modal dialogs, menus, tree views, and so on.

## Tab to the widget; use arrow keys within it

In general, the ARIA pattern can be described this way: users tab to the widget, then use the arrow keys to navigate within the widget. Sometimes other keystrokes are also available, such as Home, End, Page Up, Page Down, etc., but the arrow keys are the primary navigation keystroke within ARIA widgets.