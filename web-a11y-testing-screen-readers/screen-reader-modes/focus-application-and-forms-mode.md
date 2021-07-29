# Focus, Application, and Forms Mode

## Focus mode

Focus mode in screen readers is a mode that only allows users to navigate to focusable elements. Users cannot use the screen reader's keyboard shortcuts to navigate to semantic elements (headings, landmarks, tables, links, etc.). In screen readers like NVDA and JAWS, users can switch between focus mode and document or reading mode. Screen readers automatically switch over to focus mode when inside application regions.

## Application mode

Developers can invoke application mode by assigning role="application" to a JavaScript widget. The purpose of application mode is to allow web developers to implement all of the keyboard functionality that they need to implement in order to make the application work.

Application mode disables nearly all of the regular keyboard shortcuts in the screen reader and gives web developers a blank slate. They can create new keyboard shortcuts if they want, and implement keyboard techniques for accessing and using the application itself.

Application regions should be used sparingly, if at all, because of the way they override normal screen reader behaviors and options.

## Regular text in application mode is not readable

One of the most important drawbacks to application mode is that regular (non-focusable) text is not readable. Only the focusable elements—and their associated labels and descriptions—will be read. To ensure that text within an application is available to screen reader users, there are two main techniques:

- Associate the text with focusable elements using `aria-label` or `aria-describedby`
- Wrap the non-focusable text in a document region using role="document". Having a nested document region within an application region allows screen reader users to use their regular keyboard shortcuts within the document region portion of the application widget.

### Keep the application region small

If you do use an application region, use it only on the specific widget, and only on the part of the widget that requires custom keyboard event handlers.

## Forms mode

When in a text field in a form, users want to be able to type text in the form field. Screen readers need to disable all of the keyboard shortcuts associated with letters and numbers in order to allow users to type text. If you are using JAWS, for example, the H key normally takes you to the next heading. But when typing in a form field, you don't want to go to the next heading. You want to type the letter H. To make that possible, JAWS automatically switches from document to forms mode, disabling the normal keyboard shortcuts to allow you to type the letters and numbers.

When typing in a text field in forms mode, screen readers will speak the letter being typed (e.g. "H") and allow the character to be typed.

Screen readers generally switch over to forms mode automatically as soon as you put the focus on a form field by tabbing into it. Forms mode is not activated when simply reading through the content of a form in regular reading mode or document mode. In other words, the `<form>` tag itself does not trigger forms mode. You have to put the keyboard focus on a form field (a text `<input>`, a `<select>` menu, a `<textarea>`, a radio button, etc.) to trigger forms mode.

Some screen readers allow users to manually toggle between forms mode and document mode. In NVDA, for example, the keystroke is Insert + Space bar.

### Only focusable items—and their associated labels or descriptions—will be read when tabbing in forms

When in a form, most users will use the Tab key to navigate between focusable elements. When tabbing, the focus will not land on any non-focusable text, such as paragraphs, span elements, headings, div elements, etc. Because the focus does not land on non-focusable text, if you have any text within the form that is not focusable users may skip over that text entirely. That includes form instructions, formatting hints, and headings to group sections of the form. Users could always switch to document reading mode to hear those things, but the chances that users would do that once they're inside the form are very low. You can't count on them to ever hear any non-focusable text inside a form.

The good news is that screen readers do read the following when inside forms:

- Form labels with the `<label>` tag.
- Form labels with the `aria-label` attribute.
- Form labels with the `aria-labelledby` attribute.
- Text associated with form fields using the `aria-describedby` attribute (though there is a long delay in VoiceOver on Mac before that text is read).
- The text in the `<legend>` of the `<fieldset>`.
- The text inside links.
- The text in any element with tabindex="0".
