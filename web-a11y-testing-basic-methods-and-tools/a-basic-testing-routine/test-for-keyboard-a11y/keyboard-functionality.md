# Keyboard Functionality

## Overview

Many people cannot use a mouse and rely on the keyboard to interact with the web. People who are blind and some sighted people with mobility impairments use the keyboard or other assistive technologies that rely on keyboard commands, such as voice input. Websites need to allow people to access all content and functionality — links, forms, media controls, etc. — through a keyboard.

## Testing Methodology for Keyboard Functionality

When testing for keyboard functionality, it is important to make sure that all functionality that exists on a web page is available when using only the keyboard. Note: There are minor exceptions to this rule, such as input that relies on a user's movements (e.g., free-hand drawing); but, for the most part, functionality must be available through the keyboard. To learn more about the rules for keyboard input, browse through the course, Device-Independent User Input Methods.

To test for keyboard functionality:

- Check that you can tab to all the elements, including links, form fields, buttons, and media player controls. Make sure there are no actions or options that you cannot get to because they are only available on mouse hover or through click actions.
- Check that you can tab away from all the elements that you can tab into. A common problem is keyboard focus getting caught in controls and custom widgets and you cannot get out; it's called the "keyboard trap."
- For elements such as select boxes, sliders, or menu bars, check that you can move within the elements using the down arrow key or up arrow key. (Make sure that you can navigate within the elements without causing a change in context, such as highlighting the first item in a drop down menu automatically selects that item.)
- Be sure you can use the Enter key or Space bar to select a specific item within an element.

## Bad example

- [MarsCommuter Side](https://dequeuniversity.com/demo/mars/): the control to add another trip can only be operated by mouse
- An issue like this can be avoided when standard HTML controls such as links (<a>), buttons (<button>), and inputs (<input>) are used because they can guarantee keyboard operation.
