# Test for Landmarks

## Overview

WCAG requires that there is a mechanism for users that allows them to skip over repetitive content. This requirement can be fulfilled by providing a "Skip Navigation/to Main Content" link, semantic headings that structure the web page, or through the use of landmarks.

When landmarks are used to designate different sections on a web page, screen reader users can use the landmarks to navigate to those particular sections on the page. Using landmarks provides another way for screen reader users to jump to the main content of a web page. Landmarks can be added to a web page either by using the HTML 5 elements `<header>`, `<footer>`, `<main>`, and `<nav>`; or by using the corresponding ARIA attributes `role="banner"`, `role="contentinfo"`, `role="main"`, and `role="navigation"`.

Some best practices to keep in mind for landmarks on a web page include:

- Make sure that there is only one instance of `<header>`/`role="banner"`, `<footer>`/`role="contentinfo"`, and `<main>`/`role="main"` on the web page.
- If there are multiple instances of `<nav>`/`role="navigation"`, the sections should have unique names provided through aria-label or aria-labelledby (these unique names will be conveyed through a screen reader).
- The number of landmarks on a web page should be relatively low and appropriate for the content on the web page. For instance, if there are too many navigation landmarks, users may have a hard time figuring out the purpose of all those landmarks.

## Testing Methodology for Landmarks

Landmarks on a web page are included in the code, so they do not affect the visual design of a web page. So, the easiest and quickest way to check for landmarks is to use a screen reader. Screen readers like NVDA, VoiceOver, JAWS, and Narrator allow you to browse a web page using landmarks; but if you use NVDA, JAWS, and VoiceOver, you can also generate a list of landmarks present on the web page.

### Desktop Web

#### Option 1: Navigate by Landmarks

To navigate a web page by landmarks using a screen reader:

- Open the web page using the testing screen reader and its compatible browser (e.g., NVDA and Firefox or Chrome).
- Use the keystroke associated with navigating to the next landmark (for NVDA, D; for JAWS, R).
- If there are landmarks present, the keystroke will take you to the landmarks on the page. If there aren't any landmarks, the screen reader may announce that there is no next (or previous, if navigating backwards) landmark.
- Listen for the types of landmarks present on the page. There should be at least a landmark for the main content if landmarks are used (announced as "Main landmark") so that users can skip to the main content of the web page.

#### Option 2: Generate a List of Landmarks

Depending on the screen reader, you may generate a list of all landmarks present on the web page. For this option, we'll focus on generating a list using NVDA, JAWS, and VoiceOver.

- Open the web page using the testing screen reader and its compatible browser (e.g., NVDA and Firefox or Chrome).
- While on the web page, use the keystroke associated with generating a list of elements:
  - For NVDA, the keystroke is: Insert + F7
  - For JAWS, the keystroke is: Insert + Control + R
  - For VoiceOver, launch the Rotor using the keystroke: Control + Option + U, then use the arrow keys to find the list of landmarks.
- When you have located the list of landmarks, look to see which landmarks are available on the web page. Again, there should be a landmark for the main content for screen reader users to skip to the main content of the web page.

### Examples

- Bad: https://dequeuniversity.com/demo/mars
- Good: http://www.deque.com/blog/

## Mobile web

### Using Talkback and Firefox:

- You can either enable "Explore by Touch" (easiest for beginners) or use gestures to read and interact with the web page.
- If you use Explore by Touch, you can move your finger around the screen and the screen reader will render the content under your finger.
- For gestures, swipe right on the web page to read the next item on the web page.
- If there are landmarks on the web page, they will be announced first, followed by the content.

### Using VoiceOver iOS and Safari:

- Once you are on the web page, launch the Rotor by placing two fingers on the screen and moving them in a circular motion.
- Use left or right swipes to find the list of landmarks on the web page.
- Use up or down swipes to select a landmark from the list.
- Jump to each landmark on the web page.
