# Testing Custom Widgets

## Overview

When assistive technologies encounter web content, and custom widgets in particular, they need to be able to gather as much information as possible in order for them to effectively interact with the content.

Users need to know what they're interacting with (name), the type of element they're interacting with (role), and the state or properties of the controls they're interacting with (state or value). When standard HTML elements are used, this kind of information is conveyed rather easily to users.

However, when custom widgets are created, developers need to build this information from scratch and convey the information to assistive technology users using ARIA roles and attributes. Additionally, they have to ensure that custom widgets can be fully operated by keyboard.

So, while automated testing may help in terms of color contrast and determining if allowed values were used for ARIA roles and attributes, automated testing should only be used as a supplement to manual testing, especially for custom widgets. It is manual testing that will determine the effectiveness of keyboard accessibility and screen reader accessibility in custom widgets.

## Testing Methodology for Keyboard Accessibility and Custom Widgets

The concepts that are discussed under the Test for Keyboard Accessibility pages in this section apply to keyboard accessibility for custom widgets. The highlights for keyboard accessibility are:

- Controls must be focusable.
- The tab order must be logical and intuitive.
- Custom keystrokes must not conflict with common screen reader and browser keystrokes.
- Focus must be visible at all times.
- Focus must be managed throughout interactions.
- Content must not cause a keyboard trap.

While the above seems pretty straightforward, it must be reiterated that when it comes to custom widgets, developers must create the keyboard functionality from scratch.

So, manual testing of these widgets is critical. Also, there are certain [ARIA keyboard design patterns](https://www.w3.org/TR/wai-aria-practices-1.1/#aria_ex) that are recommended for specific widgets that developers should adhere to.

What it generally comes down to is this: Users should be able to tab to the widget and use the arrow keys within the widget. In the course, Custom JavaScript/ARIA Widgets, there are a number of widget examples along with developer and QA notes that discuss how to test each widget.

### Testing Methodology for Keyboard Accessibility and Screen Readers

When assistive technology users like screen reader users interact with dynamic custom widgets, not only do they need the widget to be keyboard accessible, but they need vital information about the widget and how they interact with the widget conveyed through their assistive technologies. In particular, assistive technology users need to know:

- The name or label of the custom widget or element. For instance, if users interact with a modal dialog, they need to know what the modal dialog is presenting to them (e.g., "Confirm Preferences").
- The role of the custom widget or element. Users need to know what type of element they're interacting with. Using the same modal dialog example, it should be conveyed to users through their assistive technology that they are interacting with a dialog.
- The state of the custom widget or element. If the state of the user interface component changes due to a user's interaction or response to it, assistive technologies need to convey the changes. A good example is an expandable region. If the user expands the region, it needs to be communicated through the assistive technology that the region is expanded.
- The properties associated with the custom widget or element. If there are attributes that contribute to the users understanding of interacting with the widget or element, these properties must be conveyed. For a slider, there is a minimum value and a maximum value that must be conveyed to users to properly interact with it.
- The value of the custom widget or element. Using the slider example again, when a user selects a value between the range provided in the slider, the value they select must be conveyed to them.

There are number of widgets and other dynamic content that developers can create. The type of information that is rendered to assistive technology users depends not only on the type of widget but also on the information related to the widget that developers include in their code.

To see how information about custom widgets is conveyed to assistive technologies, it is highly recommended that testers go to the course, Custom JavaScript/ARIA Widgets, and interact with the widget examples in the course with a screen reader. When evaluating custom widgets:

- Go through all of the content on the web page relying only on a screen reader and keyboard.
- Interact with all user interface components.
- Check that the information conveyed through the screen reader accurately conveys what is displayed as you interact with the components.
- Make sure that the information is reliable and that the components are compatible with the screen reader.
