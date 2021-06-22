# The application role

## Overview

Application mode exists to allow developers complete freedom over programming the behaviors of a widget, including keyboard event handlers.

With great power comes great responsibility though. Invoking `role="application"` requires thoughtful planning of every aspect of interaction. There are so many ways to do this wrong that most of the time it's best to avoid application regions altogether. Even so, there are some legitimate use cases.

## The application role MUST NOT be used anywhere where screen reader users need to use page navigation features.

In normal document reading mode, screen readers have a wealth of keyboard shortcuts available to allow users to read text, navigate by elements (such as headings, tables, form fields, lists, etc.), find out the spelling of words, and other functionality related to text and document structure.

Nearly all of these are turned off in an application region. Why? Because web developers need to be able to control the logic of keyboard interactions within web applications, including specifying custom keyboard shortcuts, if appropriate. If screen readers left all their keyboard shortcuts intact in an application region, the screen reader's keyboard shortcuts would interfere with the developer's keyboard logic, and scripting keyboard interactions would be nearly impossible for web developers.

The main keyboard features that are NOT disabled include the following:

- The Tab key to go through focusable items, such as links, form elements, and anything with `tabindex="0"`.
- The Enter or Return key to activate a link or button, or to submit a form.
- The space bar to activate a button or submit a form.
- The arrow keys to choose elements within `<select>` lists or to choose between radio buttons

## The document role SHOULD be used inside an application region if part of an application region requires screen reader users to navigate text content.

If you want screen reader users to be able to use their regular keyboard methods within your application, or within part of your application, you can embed role="document" inside of an application region. In other words, the following structure is allowed:

```html
<div role="application">
<div role="document">
</div>
</div>
```

This structure essentially solves the problem of not having regular screen reader keyboard shortcuts available within application regions, and it can be especially useful for modal dialogs (role="dialog" or role="alertdialog) that may have mixed content with regular text and form elements.

## Meaningful non-focusable content in an application region MUST be programmatically associated with focusable elements, or MUST be made accessible to screen readers in some other way.

No regular text is available to screen readers in application regions unless it is keyboard focusable. This means all of the following will NOT work at all for screen reader users (unless you set tabindex="0" on them to put them in the regular keyboard tab order):

- paragraphs
- headings
- `<div>` elements
- `<span>` elements
- lists
- tables
- etc.

In other words, no matter what you put in an application region, if you can't get to it with the keyboard, screen reader users won't have any access to it at all. If you have a modal dialog with a paragraph of text in it (or a table or a list or anything else not focusable), screen reader users will not hear it.

Again, there are some good reasons for this, in that the expectation is that applications will have their own keyboard logic, but you have to plan accordingly.

## Non-focusable items SHOULD NOT be made focusable just for the sake of making them readable to screen readers.

While it is true that adding `tabindex="0"` to an element makes it keyboard-focusable, thus allowing screen readers to read the text, screen reader users still can't interact with this text in the normal way. They can't read one line at a time, or one word at a time, or check the spelling of words, or do any of the other text-related operations that they're used to doing.

They can only tab to the element and listen to it in its entirety. If they pause the reader, it won't pick up where it left off. They would need to tab away from the element, then tab back to it and listen to the whole thing over again.

Also, it's not normal to be able to tab to a paragraph or a list element or a heading. Users expect some kind of link or button or form input functionality when they tab to an element. If they tab to a paragraph and then try to interact with it by hitting Enter, nothing will happen, and that might be a bit confusing. They may think something is broken.

## The application role MUST NOT be used anywhere except around a widget that requires it.

If you're going to use role="application", make sure you apply it only to the widget itself, so that screen reader users can use their normal keyboard shortcuts on the content of the web page.

Never wrap an entire web page in an application region. Specifying `<body role="application">` would be especially bad, because that renders the entire web page inaccessible by the screen reader's normal keyboard methods.

## Some widgets automatically invoke application mode

Some roles trigger application mode automatically in most screen readers, such as:

role="dialog"
role="alertdialog"
role="tablist"

You can't stop the screen reader from entering application mode on these elements, and that's by design. Just be aware that anything with these roles applied will have all the keyboard limitations for screen readers described above.

## Related Links

- [Official W3C documentation about the application role](https://www.w3.org/WAI/PF/aria/roles#application)