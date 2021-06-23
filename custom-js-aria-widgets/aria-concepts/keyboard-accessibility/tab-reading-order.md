# Tab/Reading Order

## The linear tab/reading order is determined by the DOM

The DOM (Document Object Model) can be defined as the source code after it has been interpreted by the browser and after the JavaScript has been applied. For static content, the order in the DOM is the same as the order in the original source code.

For dynamic content, though, there is a chance that the web developers might have inserted things out of order in the DOM. For example, they might throw the new code at the top of the DOM, or at the bottom of the DOM, and then rely on CSS for visual placement

That's fine for sighted mouse users, but it's not fine for keyboard users, because it's hard for keyboard users to figure out how to tab to the focusable items in the dynamic areas.

Users expect the tab order to match the visual order. When it doesn't, they often assume that the content is not keyboard-accessible at all, even if it technically is accessible but just out of order.

### Make the tab/reading order match the visual order

It is almost always best practice to make the tab/reading order match the visual order, which means ensuring that the order of the content in the DOM matches the visual order.

Users want to be able to continue through the content naturally, without having to hunt through the entire web page for the place where the focus lands on the element they're trying to access.

There are some exceptions to this rule. It can be appropriate, for example, to place the content of a modal window at the top or bottom of the DOM and then disable keyboard and screen reader access to the rest of the document while the modal is open.

Placing these self-contained sections of code at the top or bottom of the DOM isolates them from the rest of the page on purpose, so that users don't interact with the rest of the page. But for most non-modal content, you don't want to isolate elements like that.

You want them to be in the natural flow of the document, which means making sure that the DOM order matches the visual order.