# Title for Every Page

## The page `<title>` MUST be present and MUST contain text.

Screen reader users rely on the title to quickly learn the identity and purpose of the page. If you leave off the title, screen reader users will have to browse the page and infer the identity and purpose from the content, which is highly inconvenient.

## The page `<title>` MUST be updated when the web address changes.

Any time the web address changes, whether due to a true page load event, or due to an AJAX call (as in single-page applications), or due to a JavaScript event, the page <title> must change to reflect the new content. Otherwise, the page title will be out of sync with the content, which can lead to confusion, especially if the user arrives at the page via a link sent to them or saved in a bookmark.