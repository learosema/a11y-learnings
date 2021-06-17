# Dragon Naturally Speaking

Dragon Naturally Speaking (Dragon) is by far the most popular suite of voice input products. Its manufacturer, Nuance Corporation, primarily markets Dragon as business productivity software, but it is widely used by people with mobility issues that make typing or using a mouse painful, difficult, or impossible. Dragon is available for both Windows and Mac desktop platforms as well as Android and iOS on mobile platforms.

## Basic Dragon Commands

- [PDF Command List](module-guide-dragon-commands.pdf)

## Navigating with Mouse Grid

There may be times when the commands within Dragon Naturally Speaking do not work. This is often the case where the item's label is not the same as the visible on-screen text, or it has not been given appropriate name, state, or role values, or it is a custom control. 

In such a case, the mouse grid can be used to gain access to parts of the screen.

To open the mouse grid, say "Mouse Grid". An overlay will appear on the screen with numbers from 1-9 in each cell. Saying the name of the grid (for instance '3') will present a new, smaller grid in that location on the screen.

You can progressively keep saying numbers and getting smaller mouse grids until the part of the screen you wish to interact with is in the grid. For things like links and buttons you may need to go down several levels.

When you're finally at a point where you can safely click and get the thing you want, merely say "Click". Other options would be to say things like "Drag mouse left" which would drag the item (if, in fact, it is draggable).

## Dragon's support of ARIA

Starting with the release of Dragon version 13 in 2014, Dragon provides limited support for ARIA roles and properties including:

- button
- link
- radio
- checkbox
- aria-label
- aria-labelledby

So, when a user says, "Click radio button," radio buttons that are built from standard HTML input elements with a type of "radio", as well as those that have the ARIA role of "radio", will be shown with a number beside them.

Custom controls and controls that use arrow keys, such as tabs and sliders, may require the use of mouse emulation techniques such as mouse grid to operate.


## Product page

- https://www.nuance.com/de-de/dragon.html