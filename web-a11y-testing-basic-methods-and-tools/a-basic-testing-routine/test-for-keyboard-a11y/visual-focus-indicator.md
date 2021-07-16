# Visual Focus Indicator

## Overview

As users tab through links and form elements, they must be able to see where the keyboard focus is. Otherwise, they won't know when to use the enter key to follow links or when to type in information in form fields. Keyboard focus should be visible and logical through the page elements.

Testing Methodology for Visual Focus Indicator
There are a number of methods that can be used for visual focus. For instance, a vertical bar can be used when an empty text field receives focus, links can have a visible border or outline around them when they receive focus, or a button can change color when it receives focus. The goal behind testing for visual focus is to ensure users know where the keyboard focus is at all times.

## Keyboard-Only Testing

To test for visual focus indicator using the keyboard:

- Tab into the web page from the URL field in the browser.
- As you navigate through the web page, check to see that focusable elements have a clear, visible indicator that identifies visual focus.
  - Elements like links, buttons, and form controls should have a border around them or another similar indicator.
  - The browser's default focus (sometimes a dashed border or outline around the element) will suffice, even though it is best practice to enhance the focus through CSS.
- If images are used as links or if there are other types of active images, make sure they also have a visual focus indicator.
- When a text field receives focus, focus should be identified. This can be through a vertical bar or text highlighted in the field to let users know they can type. The field can also have a border or outline in addition to a vertical bar within the field.

### Note:

Find a sample bug report for visual focus indicator on the Writing Effective Accessibility Bug Tickets page under the Bug/Issue Management section of this module.

## Mouse-Only Testing

A visual focus indicator should also be available to mouse users. For instance, when a mouse user clicks into a text field, they should also see a vertical bar or some indication that the field has focus.

Additionally, if they use an element to trigger something on the web page, (e.g., a button to open a dialog or expandable region), they should see the focus on the triggering element when they close the content.

Also, a <b>visual hover indicator</b> should be provided for mouse users. A visual hover indicator helps to identify active elements on a web page like links and buttons.

For example, when hovering over a link, there should be a distinctive change in the hover state to indicate the link can be selected. Additionally, the mouse cursor should change to the hand pointer when hovering over links (but not for buttons — the mouse cursor should remain the same when hovering over buttons).
