# Custom Form Inputs

## Overview

The Custom JavaScript/ARIA Widgets module covers custom JavaScript widgets in detail, so in this module we will present only some of the highlights of what to consider when creating custom form elements

## Native HTML form elements SHOULD be used whenever possible.

Native HTML form elements are inherently accessible. You don't need to use any JavaScript to make them work correctly for keyboard users, screen reader users, or any other set of users. Native HTML form elements just work.

Not only that, but users are already familiar with native HTML form elements. You don't have to provide any instructions or worry about the user interface. There is no learning curve.

## Custom form elements SHOULD act like native HTML form elements, to the extent possible

If you decide that you have to create a custom form element, model it after native HTML form elements as much as possible, including keyboard behaviors (e.g. checkboxes are checked/unchecked using the space bar, radio buttons are selected with the arrow key, etc.).

In fact, if you're going to create a custom version of something that already exists — like a text input, checkbox, radio buttons, or textarea — users will expect it to work exactly like the native element. Pay close attention to keyboard behaviors, and duplicate the functionality exactly.

If you're creating an innovative form element that isn't quite like any native HTML form element, it's still a good idea to look to native HTML form elements as models.

Think through the use case of keyboard users. Make sure all buttons are functional with both the enter key and the space bar. Make sure arrow keys can be used where users might expect to use them.

## Custom form elements SHOULD have appropriate names, roles, and values.

The ARIA specification opens in a new window and ARIA authoring practices opens in a new window explain how to use ARIA (Accessible Rich Internet Applications) effectively to create custom widgets. Names, roles, and values are core concepts of ARIA.

### Name

The element's label (such as "volume control" or "date picker" or "Submit"), which is often assigned in ARIA via aria-label or aria-labelledby.

### Role

The element's functional purpose; the ARIA specification defines a list of roles opens in a new window to choose from (such as "dialog" or "menu" or "tabpanel").

### Value

The attributes or current state of an element (such as aria-selected="true" or aria-expanded="false" or aria-required="true"). The values must be updated when appropriate (e.g. change aria-expanded="false" to aria-expanded="true".

## Updates and state changes that cannot be communicated through HTML or ARIA methods SHOULD be communicated via ARIA live messages.

Screen readers don't understand what custom widgets are or how they are supposed to behave, so when a custom value changes, you may need to communicate that change to screen reader users via an [ARIA live region](https://www.w3.org/TR/wai-aria-1.1/#aria-live) (live announcements can include things like "table sorted by name, ascending" or "Results filtered by popularity", etc.). Screen reader users will hear the announcement.