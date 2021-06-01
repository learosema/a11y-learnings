# Incomplete Designs

## Partial solutions may not solve the problem at all

- "a little knowledge is a dangerous thing"
- knowing only a little can be just as bad as, or worse than, not knowing anything about it
- bad ARIA is worse than no ARIA

A design failure in one area can be the weakest link in the accessibility chain, causing the whole experience to fail for the user.

Not all accessibility failures are catastrophic, but when you're designing something, you really ought to know what your end goal is and how to achieve it. Usually that means that at least one person on the team has to be an accessibility expert. Not everyone has to be an expert, but they have to listen to what the expert says, and implement the techniques fully, not just partway.

## Incomplete designs in the physical world that fail completely

Sometimes individual parts of a design can be correct but the overall can still fail because nobody considered how the parts would work together. Having two accessible components that are incompatible with each other still produces an inaccessible result

- Bad example: Doors that block wheelchair ramps
- Bad example: Wheelchair ramps leading to steps

## Incomplete web a11y designs that fail completely

There are more ways to fail at accessibility than there are to succeed at it, so it wouldn't be worth it to try to come up with a list of all the possible failure scenarios, but here are a few examples:

- An inaccessible trigger for an accessible widget: a web page has a dialog which is fully accessible but the control to open the dialog is a custom JavaScript button that users cannot tab to, nor can they activate it with the enter key or space bar. -> inaccessible for keyboard users
- Applying `aria-hidden="true"` to otherwise accessible objects: A web page is designed to be fully accessible, and it would be accessible except for the fact that someone added aria-hidden="true" to some of the objects, making it so screen readers will not read them. Users can still tab to the focusable elements in those objects, but the screen reader will say nothing.
- Adding `tabindex` to focusable elements to fix bad tab order: in theory, adding tabindex to every focusable element would work, but it's bad practice and would be a pain when the content is updated through JavaScript. Also, positive tabindex numbers have a host of other problems (0 and -1 are useful when working with custom JavaScript widgets).
- An inaccessible custom JavaScript widget: If it is necessary to interact with a custom JavaScript widget to get to the next step of a process, and if that widget is inaccessible, users will be stuck. They won't be able to proceed beyond the broken widget.

