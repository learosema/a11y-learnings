# Placeholder Text as Labels

## Placeholder text MUST NOT be used as the only method of providing a label for a text input.

Many designers are tempted to use placeholder text as a replacement for a proper label. Usually placeholder text is visible in the form field until the form element receives mouse or keyboard focus — or until the user begins to type in the field — then the placeholder text disappears, to make room for the user's input.

If the placeholder text is used to convey important formatting information, such as whether to type a two- or four-digit year in a date field, users will have to delete the information already in the field to see the placeholder text again.

Additionally, if a user wants to review a form before submitting it, they may have difficulty ensuring they have entered the correct information in the correct fields if there are no visible labels once the placeholder text is gone.

Screen reader support for placeholder text has improved and all major screen readers read the placeholder text as a field label when the text field is empty. Once text has been entered, results vary among screen readers.

At this time, both NVDA and JAWS read placeholder text as the field label even when text has been entered in the field. VoiceOver, however, does not read the placeholder text as a label after text has been entered.

In short, placeholder text is not a sufficient technique for providing a label or advisory information.
