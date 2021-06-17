# The ARIA Keyboard Interaction Model

As the web has moved away from a pure document model toward a full-featured interactive application model, JavaScript programmers have sometimes struggled to come up with keyboard interaction patterns that make sense for the web.

Web interactions were typically limited to the use of the tab key and the enter key, with the arrow keys being used only rarely.

In contrast, operating systems like Windows, macOS, and Linux have had more sophisticated keyboard design patterns that take advantage of the full range of keyboard options, with extensive use of the arrow keys, as well as modifier keys like Control, Alt, Shift, Command, function keys (F1, F2, F3, etc.), and so on.

## ARIA Keyboard Best Practices

ARIA includes keyboard interaction patterns that are more in line with the desktop model, to give JavaScript programmers more flexibility, and to give users a more consistent and efficient experience across desktop and web applications. 

The WAI Authoring Practices opens in a new window documentation provides recommended keyboard interaction patterns opens in a new window for many of the most common types of JavaScript widgets such as accordions, autocomplete, modal dialogs, menus, tree views, and so on.

## Tab to the Widget; Use Arrow Keys Within It

In general, the ARIA pattern can be described this way: users tab to the widget, then use the arrow keys (not the Tab key) to navigate within the widget. 

Sometimes other keystrokes are also available, such as Home, End, Page Up, Page Down, etc., but the arrow keys are the primary navigation keystroke within ARIA widgets. Then users can tab away from the widget with a single keystroke.

In this way, ARIA design patterns also save us keystrokes: tab once to get into the object, and tab again to get out of it.

Navigating around within the object is optional and is done with the arrow keys (and sometimes other keys), but only if we want to.