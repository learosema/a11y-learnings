# Pointer Cancellation

## For functionality that can be operated using a single-pointer, at least one of the following MUST be true: no down-event, can abort/undo, up reversal, or essential.

People with various disabilities (as well as those without) can accidentally click or tap things. This rule is designed to allow users to prevent or undo any accidental actions through at least one of the following measures:

- <b>No Down-Event</b>: The down-event of the pointer is not used to execute any part of the function.
- <b>Abort or Undo</b>: Completion of the function is on the up-event and a mechanism is available to abort the function before completion or to undo the function after completion.
- <b>Up Reversal</b>: The up-event reverses any outcome of the preceding down-event.
- <b>Essential</b>: Completing the function on the down-event is essential.

The preferred and most accessible solution here is to make activation occur on the up-event.

An example of an essential exception is an on-screen piano keyboard, where the down event plays the appropriate note. Other essential exceptions are functions that emulate a keyboard or numeric keypad. Note also that this rule applies to web content that interprets pointer actions (i.e. this does not apply to actions that are required to operate the user agent or assistive technology).