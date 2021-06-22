# Operability

## Overview

First, we'll state the obvious: Keyboard accessibility requires that your website actually work with a keyboard. 

If any part of your website requires a mouse, your website isn't keyboard-accessible. That's what "operability" refers to: 

The website has to work with the user's input device and methods. The person may have a mouse, a keyboard, a touchscreen, voice activated controls, eye-gaze tracking hardware, a single-switch device that detects cheek movements, or some other kind of device... and your website needs to work with all of these.

Sadly, a large number of websites have features that work only with the mouse. This creates problems for several categories of people with disabilities, including:

- Users with tremors or spastic movements in their hands, who lack the manual precision required to use a mouse
- Users without hands who find it easier to use a device like a mouth stick with a keyboard than with a mouse
- Blind users who can use a mouse just fine, but can't see where the mouse pointer is, so it doesn't make sense for them to use a mouse.

The good news is that most of the technologies used by people who can't use a mouse emulate a keyboard, so for most things it is safe to assume that if it works with a keyboard and with a mouse, it works for essentially all kinds of input devices.

There are a few exceptions when you get into touchscreen gestures or other specialized methods. In those cases, you would need to do a few extra things to make the gestures work, but you would still want to make sure the actions work with a keyboard alone, or with a mouse alone.

## How to test keyboard accessibility

There is really only one way to test keyboard accessibility and that is to set aside your mouse and try to do everything on your website with just a keyboard. Here are some basic keyboard methods:

- Focus: Make sure that actionable items can receive keyboard focus, including:
  - Links
  - Form elements
  - Buttons (including "close" buttons on popups)
  - Drop-down menus
  - Tooltips and mouse-over actions
  - Modal windows and popups
  - Drag and Drop controls and objects
  - Media player controls (play, pause, volume, captions, resize, etc.)
  - Custom controls (simulated checkboxes, radio buttons, select lists, etc.)
  - Type-ahead or predictive text fields
  - Date pickers
  - Anything that users need to interact with, or that hides information from users until they request it
- Functionality: All of the controls need to perform the correct action in the expected way. For example:
  - Buttons (including submit buttons, radio buttons, and checkboxes) need to be capable of being activated with the mouse, the enter/return key, AND the spacebar.
  - Links need to be "clickable" with the mouse and the enter/return key
  - Radio buttons need to be "tabbable" as a group, but you use the arrow keys to navigate between radio buttons in the group
  - Drop-down select lists should be usable with the up and down arrow keys, or the user should be able to use alt + down arrow to expand the list, then use the arrow keys within the list, and use the enter/return key to select the option.
  - ARIA widgets should follow the design patterns outlined in the [ARIA authoring practices](https://www.w3.org/TR/wai-aria-practices-1.1/)