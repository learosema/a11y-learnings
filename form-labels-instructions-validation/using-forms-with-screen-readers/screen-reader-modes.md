# Screen Reader Modes

## Overview

Most screen readers have different modes that apply to different sets of circumstances. The two biggest categories of circumstances are:

- Page navigation: When the user needs to navigate around within the document, all kinds of keystrokes are available for a wide variety of tasks (e.g. H for headings, G for graphics, T for tables, etc.). This page navigation mode is also referred to as scan mode (in Narrator), browse mode, or document mode.
- Input or interaction: When interacting with an element — such as when typing in a text field, or when inside a custom JavaScript widget — it would be bad if the H key took users to the next heading, so screen readers suppress page navigation keystrokes under those circumstances. This interaction mode has a few variations and names, including forms mode, focus mode, and application mode.

Below we'll explore the differences between page navigation in terms of document mode and how screen readers interact with forms in forms mode.

## Forms mode

When in a text field in a form, users want to be able to type text in the form field. Screen readers need to disable all of the keyboard shortcuts associated with letters and numbers in order to allow users to type text.

If you are using JAWS, for example, the H key normally takes you to the next heading. But when typing in a form field, you don't want to go to the next heading. You want to type the letter H.

To make that possible, JAWS automatically switches from document to forms mode, disabling the normal keyboard shortcuts to allow you to type the letters and numbers.

When typing in a text field in forms mode, screen readers will speak the letter being typed (e.g. "H") and allow the character to be typed.

Screen readers generally switch over to forms mode automatically as soon as you put the focus on a form field by tabbing into it. Forms mode is not activated when simply reading through the content of a form in regular reading mode or document mode. 

In other words, the `<form>` tag itself does not trigger forms mode. You have to put the keyboard focus on a form field (a text `<input>`, a `<select>` menu, a `<textarea>`, a radio button, etc.) to trigger forms mode.

Some screen readers allow users to manually toggle between forms mode and document mode. In NVDA, for example, the keystroke is Insert + Space bar.

## Only focusable items—and their associated labels or descriptions—will be read when tabbing in forms

When in a form, most users will use the Tab key to navigate between focusable elements. When tabbing, the focus will not land on any non-focusable text, such as paragraphs, span elements, headings, div elements, etc. Because the focus does not land on non-focusable text, if you have any text within the form that is not focusable users may skip over that text entirely. 

That includes form instructions, formatting hints, and headings to group sections of the form. Users could always switch to document reading mode to hear those things, but the chances that users would do that once they're inside the form are very low. You can't count on them to ever hear any non-focusable text inside a form.

The good news is that screen readers do read the following when inside forms:

- Form labels with the `<label>` tag.
- Form labels with the aria-label attribute.
- Form labels with the aria-labelledby attribute.
- Text associated with form fields using the aria-describedby attribute (though there is a long delay in VoiceOver on Mac before that text is read).
- The text in the `<legend>` of the `<fieldset>`.
- The text inside links.
- The text in any element with tabindex="0".

## Document/Browse/Scan Mode

### Reading text

In document mode, or reading mode, screen reader users are able to read text, navigate by words, navigate by characters to hear the spelling of words, and so on. This is the default mode of most screen readers.

### Navigating by semantic elements

When users want to navigate by semantic elements — such as headings, landmarks, tables, graphics, lists, links, etc. — they can use the screen reader's keyboard shortcuts to go forward or backward through those elements.

- In JAWS and NVDA, document mode or reading mode is the same mode that allows them to navigate by semantic elements.
- In Narrator, users need to enter into "Scan Mode" (by pressing Caps lock + Space bar) to navigate by semantic elements.
- In VoiceOver for macOS, there is no need to switch modes, because VoiceOver doesn't have the same concept of modes as other screen readers.

## Other Modes

There are other types of modes that screen readers use to navigate online content. While this page just highlights these other modes, you can learn more about these different modes in Module 2: Using Screen Readers.

### Focus mode

Focus mode in screen readers is a mode that only allows users to navigate to focusable elements. Users cannot use the screen reader's keyboard shortcuts to navigate to semantic elements (headings, landmarks, tables, links, etc.).

For instance, forms mode is a type of focus mode for screen readers where users tab to form elements and certain shortcuts are disabled so users can interact with the form.

In screen readers like NVDA and JAWS, users can switch between focus mode and document or reading mode. Screen readers automatically switch over to focus mode when inside application regions.

### Application mode

Developers can invoke application mode by assigning role="application" to a JavaScript widget. The purpose of application mode is to allow web developers to implement all of the keyboard functionality that they need to implement in order to make the application work.

Application mode disables nearly all of the regular keyboard shortcuts in the screen reader and gives web developers a blank slate. So, screen reader users can't use keyboard shortcuts that are normally available to them like "H" to navigate by headings.

Developers can create new keyboard shortcuts if they want, and implement keyboard techniques for accessing and using the application itself. Because application mode overrides normal screen reader behaviors and options, it should be used sparingly and only on specific widgets and parts of widgets that have custom keyboard handlers.

### Table Mode

Screen readers allow users to navigate through tables in any direction: right, down, left, and up. When using the proper keystrokes, the experience is much like navigating through the cells in a spreadsheet. All Windows screen readers use Control + Alt + Arrow keys for table navigation; on macOS it is Control + Option + Arrow keys.

## Switching Modes in Screen Readers

Some screen readers have the capability to switch between modes. The table below presents the keystrokes used for common screen readers to switch between modes like document mode and forms mode.

### Methods to switch modes

- Narrator: Caps lock + space bar (turns scan mode on or off)
- NVDA: Insert + Space bar (switches between document mode and focus mode)
- VoiceOver for macOS: no need to switch modes
