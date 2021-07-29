# Screen Readers Read the Accessibility API and/or DOM

Screen readers don't read the raw HTML source code of the web page. They read the content after it has been parsed by the browser, which means after JavaScript and styles have been applied to the page.

This is good, because many modern websites require JavaScript and styles in order to work at all. If screen readers only read the original source code without the JavaScript and styles, blind users would experience a very broken web.

The DOM can be static, but most commercial websites these days include dynamic elements that update and change the DOM on the fly after the page has loaded. Screen readers can read these changes, but screen readers do not automatically announce the changes.

Screen readers will simply read whatever the current DOM says. If, for example, the bottom paragraph of the web page on load says "Hello World" and then changes to "Hello Universe" before the screen reader gets that far, the screen reader will say "Hello Universe" (the updated text) when reading that paragraph.

In fact, the screen reader will never know that the last paragraph used to say "Hello World." That may or may not be a problem, but the point is that the screen reader reads the current DOM, not necessarily the original DOM.
