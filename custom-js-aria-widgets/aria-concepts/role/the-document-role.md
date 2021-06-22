# The Document Role

## Overview
When in a document region, screen readers allow users to use keyboard shortcuts to navigate by elements (headings, landmarks, tables, lists, etc.), and allow users to access all aspects of the text, including the spelling of words.

### Note:
The default role for a web page is the document role, so you don't need to do anything to a standard web page to give it that role. The web page is already the equivalent of role="document".

The only reason to actually write `role="document"` is to create a document region inside some other type of region, such as within an application region. An example would be creating a document region inside of a modal dialog (a container with role="dialog", which is a special kind of application region) so that screen reader users can navigate and read the text inside the dialog. 

If you put regular text (paragraphs, headings, `<div>` elements, lists, tables, etc.) in a dialog, screen readers can't access it, because only keyboard-focusable items (and their programmatically-associated labels and descriptions) are accessible in application mode.

## Related Links

- [Official W3C documentation about the document role](https://www.w3.org/WAI/PF/aria/roles#document)