# Checklist for Designers

This checklist is the starting point for an accessible design, not the end point. These are highlights of some of the most important concepts. Push yourself to think beyond the bare minimum, to create designs that people with disabilities actually like, and that they find useful and well-suited to their needs.

## Page Title

- Does the page title (the browser title for the page; not the main content heading or `<h1>`) describe the topic or purpose of the page?

## Headings

- Is all text that looks and acts like a heading marked as a heading?
- Are the heading levels chosen so they convey their correct hierarchical order in the content, not for their visual styling?

## Navigation

- Is a method provided to skip repetitive navigation and go to the main content? Two of the main techniques including providing HTML/ARIA landmarks (e.g. header, navigation, main, footer), and "skip navigation" links.
- Will the content's reading and focus order, as determined by the code order, be logical and intuitive?

## Links

- Does link text clearly describe the purpose or destination of the link?

## Color/Contrast

- Is information conveyed by means other than just color alone? For example, using color and text both to indicate that a form field has an error, or using colors with text to label chart categories.
- Does all text have a minimum color contrast against its background of at least 4.5 to 1 (3 to 1 for large text)?
- Is link text distinguishable from non-link text by more than just color?
- Do actionable elements have clear, visible focus when non-mouse users Tab or Arrow to them?
- Do all non-text elements (user interface components and graphical objects) that are important for accessing and understanding content have sufficient color contrast of at least 3 to 1?

## Magnification and Responsive Design

- Can a user with low vision magnify or zoom in on the content in the browser on any device, including desktop and mobile?
- Is the design optimized for all zoom states? Simplify the design as much as possible, eliminating horizontal scrolling.
- Can a user use the website with their device in their preferred orientation (landscape/portrait)?

## Images

- Does the alternative text for informative images provide the same information as the image?
- Does the alternative text for actionable images, such as an image link, button, or image map area, clearly identify the link destination or button purpose?
- Are complex images or infographics explained fully in the page content and with a short alternative text description?
- Are decorative images identified as not requiring alternative text?
- Is plain text used instead of text embedded in images? (exceptions like text in logos and decorative text images exist)

## Tables

- If the page contains a data table, does the table have a caption (name/title), and are columns and/or rows properly identified in the markup?
- Are complex tables simplified to minimize or eliminate the need for compound column or row headers?

## Forms

- Do all form fields have a label that is always visible?
- Are all form labels adequately descriptive and instructive? Is all the information the user needs to fill out the form available on the page?
- Are all form labels and instructions immediately adjacent to their form element so that users (including users of screen magnification) can easily connect the form element with its label and/or instructions?
- Are all controls in close proximity to the content they are controlling? For example, are Edit and Delete buttons next to the content they modify?
- Do error messages provide enough information for users to correct their error?
- Are forms written so they can be used with Autofill?

## Dynamic Content

- Are users made aware of content that is dynamically inserted on a page or does the new content come right after the element that caused it to appear, in the logical reading order / tab order of the page?
- Do all keyboard-only and touch screen interactions follow expected patterns so users know how to interact with all widgets on the page?
- Design success and failure feedback into all interactions. When users activate scripted functionality (buttons, form submissions, etc.), they must know whether the action was successful or not, through a success/error message, the obvious activation of a feature (e.g. a video starts to play after the user activates the "play" button), etc. The feedback must be available to sighted users, screen reader users, and all other user categories.

## Custom Widgets

- Does the design use standard HTML widgets (links, buttons, form elements, controls, etc.) whenever possible? Native widgets have built-in accessibility capabilities. Custom widgets do not.
- If you do have any custom widgets, have they been created with full keyboard support, and are they compliant with WAI-ARIA authoring practices?

## Touch Devices

- Is the touch target size of main links and buttons large enough and far enough apart from each other to activate easily with a finger?
- Is there an alternative way to activate any custom swipe actions or gestures? Note that when a screen reader is activated on a touch device, - it overrides all custom swipe actions and gestures.
