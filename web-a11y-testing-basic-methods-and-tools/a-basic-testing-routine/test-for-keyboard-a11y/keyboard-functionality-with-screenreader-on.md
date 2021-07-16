# Keyboard Functionality with Screen Reader On

## Overview

Screen reader users rely on specific keystrokes to navigate and interact with the web page. So, it is critical to make sure that the common keyboard shortcuts available to them through the screen reader are not in conflict with any custom keyboard shortcuts created by developers.

Additionally, existing keystrokes available through the web browser and operating system must not conflict with any custom keystrokes.

## Screen Reader Modes

In order to use the keyboard effectively, screen readers have different modes for using and interacting with web pages. There is a specific purpose for each mode and each mode has a different set of operations for interacting with a web page.

The modes available to use for most screen readers are:

- Document (Reading) Mode: Usually the default mode for screen readers where screen reader users can read text and navigate by words and characters.
- Focus Mode: A mode that allows screen readers to navigate by focusable elements (using Tab key or arrow keys). Some keystrokes that are available in document mode are not available in this mode.
- Application Mode: A mode that disables all the regular keystrokes for screen readers and allows developers to create custom keystrokes (should only be used for specific custom widgets).
- Table Mode: A mode that allows users to navigate tables in any direction of their choosing.

Learn more about using screen readers through the course, Using Screen Readers.

## Testing Methodology for Keyboard Functionality with a Screen Reader

To test for keyboard functionality with screen reader:

- Open the web page using a screen reader and its compatible browser (it will be wise to test with multiple screen readers and browsers).
- Navigate into the web page from the URL field using the Tab key.
- While browsing through the web page, use some of the common keystrokes available to screen reader users (for instance, H for headings, G for images).
- If possible, locate elements like a table or a form to use keystrokes available in different modes (table mode, forms mode). Check that the keystrokes available in those specific modes are functional.

## Bad Example

The link in this example takes you to a form that uses the keystroke G to submit the form. Screen reader users navigate images and graphics on a web page using the G keystroke, so the shortcut used to submit the form interferes with the keystroke screen reader users are accustomed to using to navigate graphics.

When you are not using a screen reader, the form submits any time you use the G key. However, when you use a screen reader like Narrator or NVDA, the screen reader will look for graphics on the page when the G key is used.

- [Bad keyboard shortcut example](https://dequeuniversity.com/assets/html/module-input-methods/keyboard-shortcuts/badkeyboardshortcut.html)

The issue with the form is that a developer assigned form submission to the G key, but it doesn't work when a screen reader is in use. A screen reader's keystrokes will override custom keystrokes if the keystrokes clash. It is important to report this information if this issue is discovered in testing.
