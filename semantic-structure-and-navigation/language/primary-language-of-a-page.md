# Primary Language of a page

## The primary language of the page MUST be identified accurately on the `<html>` element.

If the language is not specified, or if it the language designation is inaccurate, a screen reader will read the document in the user's default language, which may result in a very bad accent if the page language doesn't match the user's default. In fact, it can be very difficult to understand anything when screen readers are using the wrong language library.

## The primary language of the page MUST be identified with a valid value on the `<html>` element.

The language designation must come from a standard list of language codes, which includes en (English), fr (French), es (Spanish), and others, according to the specification. Anything else (such as lang="English") will not work.

Some screen readers support only two-letter codes. Other screen readers support regional language codes, such as en-us (American English) or fr-ca (French Canadian).

