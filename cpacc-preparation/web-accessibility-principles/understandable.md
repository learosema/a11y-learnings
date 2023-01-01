## Understandable

## Defining Understandability

Understandability is about making content and interfaces that people can comprehend.

## Understandable Content


### Specify the Language

Screen readers convert digital text into synthesized speech—they read the text aloud—or into braille output for use in a refreshable braille device. If language of the web page is not designated in the markup (for example: `<html lang="en">`), the screen reader will read using the pronunciation rules of whatever language is specified in the user's default settings.

That's fine if a user speaks only one language and visits pages in only that language, assuming that the user correctly sets the default language in the screen reader. If a user speaks two languages, though, and visits web sites in both languages, the screen reader will not automatically switch between languages unless the web page itself specifies which language to use.

If the screen reader uses the wrong pronunciation rules, it will sound awful, and will not be understandable. In order to hear the web content read correctly, the user will have to change the language setting every time when going back and forth between this page and other pages in other languages.

That's an inconvenience that web developers can prevent, by specifying the language in the markup. It is also possible to mark words, phrases, or passages of text within a page as a different language (for example: `<span lang="fr">Je parle français</span>`).

### Simplify the Reading or Vocabulary level

Reading is hard for some people. Reading disorders are quite common, so even though it can actually be quite hard to simplify your writing, it can be worth it for people with reading disabilities. The kinds of things that are difficult include:

- long or unfamiliar words
- long sentences
- complex sentence construction
- unclear wording
- long passages of text (it's usually best to break up text into sections with headings, shorter paragraphs, and lists, where appropriate)
- lines of text that are too close to each other (it's usually best to include some blank visual space between lines of text)

There are other considerations as well, but these are a good start.

### Limit or Avoid Terminology or Concepts that are Unfamiliar or Complex

Unfamiliar technical jargon or slang can be confusing. Culturally-specific words or concepts can also be confusing or easily misunderstood because the person does not have the necessary cultural heritage or education to understand the context.

Some people with more generalized cognitive disabilities are unable to understand complex ideas and abstractions. The more you can simplify the content, the better for these individuals.

### Provide Supplemental Formats

Some people can't read at all. No amount of simplifying of the reading level of the text will make the text any more readable to people whose brains can't process text. For these people, you need to provide alternative formats, such as images, audio, or video, and those alternative formats would need to present the content as directly and as simply as possible.

If creating all of those alternative formats sounds like it would take a lot of work, that's because it would. If your main audience is people who can't read, then you would need to do this, but for general audiences you would not. Accessibility guidelines don't require you to go to this level of extreme accessibility.

It's true that some people need it, but we have to be realistic and acknowledge that converting all text to images, audio, or video would be an undue burden on most organizations. Even so, the principle remains valid: providing supplemental formats can benefit people with various kinds of cognitive disabilities. In fact, there is some evidence that people have different styles of learning based at least partially on different sensory modalities.

Those with a verbal or linguistic style of learning will likely process text well. Those with a visual or spatial style of learning will benefit from pictures and video content. Those with an aural or auditory-musical style of learning will benefit from audio versions of content, or from multimedia videos.

## Understandable Interfaces and Interactivity

### Consistency and Predictability

Web sites with multiple pages or views should maintain a consistent look and feel across the pages or views. The visual layout and underlying reading order and tab order should not change radically from one page to another within the same context. The main navigation should generally contain the same links (though some links in submenus may be hidden in some views) and the text in those links should be consistent.

Form controls, custom controls, and custom widgets should behave in standard ways, in accordance with common conventions. It is generally a bad idea to design a completely new and different way of interacting with web components unless there is a compelling reason, or as an experiment. Even then, you would probably need to provide some additional instructions to let users know how to use the new components.

## Assistance: Error Prevention and Correction

### Provide Instructions, Hints, and Contextual Help

When asking for user input, it is often appropriate to provide instructions at the beginning of the interaction, for example at the top of a form, explaining the purpose of the interaction, and what the user should do.

If a field has any special constraints, these constraints should be visibly noted next to the field and should be communicated to screen reader users. Constraints can include such things as:

- A field is required
- A button is read-only or disabled
- The data must be in a certain format
- A password must be a minimum number of characters and/or it must consist of both numbers and letters, or must have an uppercase letter, or must have a special character, etc.
- The total number of characters cannot exceed a certain threshold
- And others

### Provide Feedback with Confirmation and Error Messages

When a user submits a form or interacts with a component in a way that submits data to a server, confirm that the interaction has taken place, and tell the user whether it was successful or not. Always ensure that the confirmation and error messages are available to both sighted users and blind screen reader users.

In most circumstances, the message should be read immediately to screen reader users, without requiring them to hunt for the message or to bypass long passages of navigation or text. You can notify screen readers by sending the focus immediately to the message or by placing the message in an alert dialog.

## See Also:

- The official Web Content Accessibility Guidelines, [Principle 3: Understandable.](http://www.w3.org/TR/WCAG20/#understandable)