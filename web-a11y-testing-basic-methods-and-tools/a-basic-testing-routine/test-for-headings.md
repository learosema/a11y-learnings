# Test for Headings

## Overview

Web pages often use visual headings to identify and describe sections of a web page. It is important, though, that visual headings are also conveyed semantically as headings. The use of semantic headings not only provides a clear structure for the web document, but assistive technology users can use semantic headings to navigate the web page and learn about the content on the web page. Below is a list of items to keep in mind when evaluating a web page for headings:

- Headings are used: The page has a heading. In almost all pages there should be at least one heading, usually at the beginning of the main content, after the navigation.
- Real headings: Make sure headings use real heading markup (`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`), and not just visual styling that looks like headings.
- No misuse of headings: All text that is marked up as a heading is really a conceptual section heading. If the text isn't really serving the purpose of a heading, it shouldn't be marked as a heading.
- Heading hierarchy: The heading hierarchy is meaningful. Ideally the page starts with an "h1" — which is usually the same as or similar to the page title — and does not skip levels; however, these are not absolute requirements.

### Note:

The ARIA attributes `role="heading"` and aria-level can be used to semantically identify headings. However, it is recommended that HTML markup for headings is used.

## Testing Methodology for Headings

Though headings may be visible on a web page, it is important to determine if semantic headings are used on the web page. Like with landmarks, testers can use a screen reader either to navigate the web page by headings or generate a list of headings available on the web page.

### Desktop Web

#### Option 1: Navigate by Headings

To navigate a web page by headings using a screen reader:

- Open the web page using the testing screen reader and its compatible browser (e.g., NVDA and Firefox or Chrome).
- Use the keystroke associated with navigating to the next heading (for NVDA and JAWS, H).
- If there are headings present, the keystroke will take you to the headings on the page. If there aren't any headings, the screen reader may announce that there is no next (or previous, if navigating backwards) heading.
- Listen for headings and heading levels present on the page. There should be at least one (and only one) heading level 1 present for the entire page, and the heading level 1 should take users to the main content so that users can skip to the main content of the web page.
- Check the hierarchy of the headings used on the page. Is heading level 1 followed by a heading level 2? Do you encounter heading level 3 after heading level 2?
- Also, check to see if headings are accurate and informative. A heading should briefly highlight or describe the information contained within the section it is labeling.

#### Option 2: Generate a List of Headings

Depending on the screen reader, you may generate a list of all headings present on the web page. For this option, we'll focus on generating a list using NVDA, JAWS, and VoiceOver.

- Open the web page using the testing screen reader and its compatible browser (e.g., NVDA and Firefox or Chrome).
- While on the web page, use the keystroke associated with generating a list of elements:
  - For NVDA, the keystroke is: Insert + F7
  - For JAWS, the keystroke is: Insert + F6
  - For VoiceOver, launch the Rotor using the keystroke: Control + Option + U, then use the arrow keys to find the list of headings.
- When you have located the list of headings, look to see what headings are present on the web page. Again, there should be at least one heading level 1 for the main content for screen reader users to skip to the main content of the web page, headings should be in a proper hierarchy, and meaningful text should be used for each heading.

### Note

Keep in mind that only semantic headings are available to screen readers. So, if there is text on a web page that is styled as a heading but cannot be browsed to using the keyboard shortcut for headings or is not present in the list, that heading does not have the proper semantic markup.

### Examples

- Bad: https://dequeuniversity.com/demo/mars

## Mobile Web

### Using Talkback and Firefox:

- You can either enable "Explore by Touch" (easiest for beginners) or use gestures to read and interact with the web page.
- If you use Explore by Touch, you can move your finger around the screen and the screen reader will render the content under your finger.
- For gestures, swipe right on the web page to read the next item on the web page.
- Once you encounter a heading, make sure it is announced as a heading.
- Make sure that everything that looks like a heading is interpreted as a heading.

### Using VoiceOver iOS and Safari:

- Once you are on the web page, launch the Rotor by placing two fingers on the screen and moving them in a circular motion.
- Use left or right swipes to find the list of headings on the web page.
- Use up or down swipes to select a heading from the list.
- Make sure all headings on the web page are announced as headings and are included on the list.
