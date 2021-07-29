# Browsers

## Browser accessibility architecture

In addition to the accessibility API of the operating system, browsers must have their own internal accessibility architecture. Browsers construct an accessibility tree, which is similar in concept to the document object model (DOM), but with a more specialized purpose. Not every node in the DOM is meaningful for accessibility purposes. A `<div>` or a `<span>` element, for example, would have no semantic meaning and so wouldn't contribute anything to the accessibility tree. On the other hand, semantic elements—such as headings, tables, landmarks, lists, links, etc.—are meaningful to screen readers, so they are included in the accessibility tree. The accessibility tree contains information about objects including the following:

### Name

The text label given to the element. Sometimes the name is the text within the element itself (e.g., link text or heading text). Other times the name must be assigned with either an HTML method (e.g., `<label>` elements for form fields or `<caption>` elements for HTML tables), or via an ARIA attribute (i.e., `aria-label="This is the name"` or `aria-labelledby="someID"`).

### Description

Extra information about an element (e.g., as defined by `aria-describedby="someID"` or by the title attribute, depending on the context).

### Role

The semantic meaning of the element, which can come from native HTML elements (e.g., headings, tables, lists, etc.) or ARIA roles (e.g., `role="tablist"`, `role="tab"`, `role="tabpanel"`, etc.).

### Property

Characteristics of an element (e.g., `aria-haspopup="true"`).

### Relationship

Each relationship generally follows one of these patterns:
Parent-child hierarchies, which are often defined by the natural hierarchy of the DOM. For example, an HTML list item (`<li>`) must belong to a list (`<ul>` or `<ol>`), and an ARIA tab must belong to a tablist.
The explicit linking of an element to the element it belongs to or controls (e.g., as defined by `aria-owns="someID"` or `aria-controls="someID"`).

### State

The current condition of an element (e.g., `aria-expanded="false"` or `aria-selected="true"`).

## Internet Explorer

Internet Explorer mostly makes use of Microsoft's older accessibility API, MSAA. MSAA alone doesn't provide all the information that screen readers need, so screen readers often rely on additional methods beyond MSAA to make Internet Explorer accessible. Screen readers compatible with Internet Explorer include JAWS and (to a lesser extent) NVDA.

## Firefox

Firefox on Windows works well with NVDA and JAWS.

Firefox on Android works well with Talkback.

Firefox on macOS does not work well with VoiceOver. The implementation of accessibility features is very incomplete on macOS.

For more information, refer to the documentation about [Firefox's accessibility architecture](https://developer.mozilla.org/en-US/docs/Mozilla/Accessibility/Accessibility_architecture).

## Safari

Safari, on both macOS and iOS, takes full advantage of the macOS accessibility API.

Use the [XCode Accessibility Viewer](https://developer.apple.com/library/content/documentation/Accessibility/Conceptual/AccessibilityMacOSX/OSXAXTestingApps.html) to expose the accessibility tree in macOS. Note that XCode, which is a suite of developer tools, is not installed by default. [More information about XCode.](https://developer.apple.com/xcode/)

## Chrome

Chrome has good accessibility support; on Windows, JAWS utilizes Chrome's accessibility API well, and NVDA is likewise compatible with Chrome.

## Edge

The Edge browser makes use of the UI Automation API. The Narrator screen reader and (to a lesser extent) NVDA support Edge very well.

For more information, refer to

- the Microsoft Edge team's blog entry entitled [Accessibility: Towards a more inclusive web with Microsoft Edge and Windows 10](https://blogs.windows.com/msedgedev/2015/09/25/accessibility-towards-a-more-inclusive-web-with-microsoft-edge-and-windows-10/#GPdAwhVe0dh7BdSM.97),
- to the [documentation about Edge's F12 Accessibility Tools](https://docs.microsoft.com/en-us/archive/microsoft-edge/legacy/developer/) (obsolete)
