# Using `tabindex` correctly

## Use `tabindex="0"` to make an element tabbable and focusable

If you assign `tabindex="0"` to an element that would not normally be tabbable — like `<p>`, `<h2>`, or `<div>` — that element becomes part of the normal tab flow. Users will be able to use their tab key to put the keyboard focus on the element.

Normally you would not want to do this — it doesn't make much sense to tab to a regular paragraph, for example — but it can be a useful technique in a number of situations:

- To add keyboard functionality to legacy code with mouse-only JavaScript events.
- To add keyboard functionality to certain kinds of elements in ARIA/JavaScript widgets, such as the tabs in a tab panel (`<li role="tab" `tabindex="0"`>`).
- To force screen readers to read text inside a form or application that might otherwise be skipped. Note: There are usually better ways of ensuring text can be read in these situations, such as using `aria-label`, `aria-labelledby`, or `aria-describedby`, but `tabindex="0"` can sometimes be an acceptable workaround.

## Use `tabindex="-1"` to make an element focusable by JavaScript (but NOT tabbable)

If you assign `tabindex="-1"` to an element, users still won't be able to tab to it, but you will be able to send the focus to the element using JavaScript. This technique can be useful for a variety of situations:

- To send the focus to a message — such as an error message or confirmation message — to ensure that sighted users see it and that blind users hear it through their screen readers.
- To send the focus to a control in a JavaScript widget, such as to an inactive tab in a tablist. Before receiving the focus, the inactive tab would be set to `<li role="tab" `tabindex="-1"`>`. After receiving focus, you would use JavaScript to change the tabindex value to 0 (`<li role="tab" `tabindex="0"`>`), which would put the active tab in the normal tab flow. The other tabs (all inactive) would all be set to `<li role="tab" `tabindex="-1"`>`.

## Don't use tabindex with positive numbers

When you use tabindex for positive numbers (such as `tabindex="1"` or `tabindex="2"`), these will be the first things that the user tabs to in the page.

That puts things out of order in terms of the normal tab flow. The idea of altering the tab order isn't bad in and of itself. It may be legitimate on some web pages to send the focus to a certain area on page load.

There are two main problems with tabindex of positive numbers:

### The normal tab flow is broken:

The elements with tabindex are no longer part of the normal tab flow when cycling through the document. For example, if there are 100 links on the page, and if link 30 has `tabindex="1"` and link 31 has `tabindex="2"`, the user will first tab to link 30, then to link 31, then to links, 1, 2, 3, and so on.

So far so good, but when the user arrives at link 29, the next item they tab to will not be link 30. It will be link 32. Users will not be able to tab to links 30 or 31 until after tabbing to link 100. 

After link 100, they will go to link 31, then 32, then back to 1. It can be very frustrating to be on link 29, and to try to get to link 30, and to not be able to (at least not until hitting tab about 70 more times).

### Dynamic content may break your intended tab flow: 

Using the same example as above, of a page with 100 links, with links 30 and 31 having tabindex of 1 and 2, respectively, if you use JavaScript to insert a new section of content in between links 30 and 31, you will need to put a tabindex value on every link and every form element between that occurs after link 30 and before link 31 in order to put those elements in the normal tab flow.

If you forget to put a tabindex value on even one of them, the user will go to link 1, and will not return to that area until tabbing through links 2, 3, 4, etc., all the way up to link 29.

At that point, the user will go to the next item in the new section, but by then the user will probably be quite frustrated, and it's possible the user will just assume that link or form element is not accessible at all.