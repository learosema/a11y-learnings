# Tab Focusability and Tab Order

## Overview

When a user navigates a web page using the keyboard, he or she should be able to tab to elements that should naturally receive keyboard focus (e.g., links and buttons). Additionally, the tab order should be consistent with the layout of the content. Though the tab order should follow the reading order of the web page, it sometimes may be slightly different from the reading order of the content. As long as the tab order is logical and intuitive, though, it will allow users to understand and interact with the web page appropriately.

### Testing Methodology for Tab Focusability

To check for tab focusability:

- Start with placing the cursor into the address bar or URL field in the web browser.
- From there, using the keyboard only, navigate into the web page using the Tab key.
- As you tab through the web page, make note of elements that receive keyboard focus.
- Navigate backwards using Shift + Tab.
- Ensure all focusable elements actually receive keyboard focus. Any links, form inputs, interactive controls, and buttons should all receive keyboard focus.

### Testing Methodology for Tab Order

To check the tab order of a web page:

- Start with placing the cursor into the address bar or URL field in the web browser.
- From there, using the keyboard only, navigate into the web page using the Tab key.
- As you tab through the web page, check that the tabbing order makes sense according to the content on the web page. It is best practice for the tab order to follow the reading order of the web page.
- Tab all the way through the document to ensure the tab order is logical and intuitive.

### Bad Example: Page with illogical tab order

- [MarsCommuter demo site](https://dequeuniversity.com/demo/mars/)
