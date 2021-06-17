# Keyboard shortcuts

## Page-specified shortcut keys and accesskeys MUST NOT conflict with existing keyboard shortcuts in the browser, operating system, or assistive technologies.

When page-specified shortcuts or accesskeys are created for a web page, those shortcuts and accesskeys must not interfere with keyboard shortcuts used in the browser or keyboard shortcuts used through assistive technologies.

If a page-specified shortcut or accesskey conflicts with an assistive technology like a screen reader, the screen reader will generally override the shortcut or accesskey, making the custom shortcut unavailable to screen reader users.

For instance, when JAWS and NVDA are in document mode, they will override the custom keyboard shortcut. But when these screen readers are in application mode, they allow the web page to specify the keyboard shortcuts. Also, forms mode for these screen readers permit users to type characters.

So, page-specified shortcuts and accesskeys are an issue when custom keyboard shortcuts conflict with keyboard shortcuts used in document mode for JAWS and NVDA. Similar to JAWS and NVDA in document mode, custom keyboard shortcuts are an issue when they conflict with the keyboard shortcuts used in Narrator's scan mode.

As for VoiceOver, conflicting custom keyboard shortcuts are problematic if the screen reader user has enabled single-key navigation.

### Bad example

The keystroke `G` is used in Narrator or NVDA to navigate through graphices. The bad example overrides the `G` stroke, making the shortcut inaccessible to screen reader users.

- [Bad example, overriding the G keystroke](https://dequeuniversity.com/assets/html/module-input-methods/keyboard-shortcuts/badkeyboardshortcut.html)
