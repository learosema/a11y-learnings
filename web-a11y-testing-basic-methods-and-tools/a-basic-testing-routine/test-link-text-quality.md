# Test Link Text Quality

## Overview

When users come across a link on a web page, they expect to understand the purpose of the link. Links should be meaningful and descriptive so users know right away where links will take them without having to activate them. Text provided for the link (text within the anchor tag) should convey either the topic or content of the target page. When the link text itself doesn't convey this information, the information should be conveyed through the text immediately surrounding the link. For instance, if the link is contained in a sentence or paragraph, users should be able to gather meaningful information about the link's target page from the text within the sentence or paragraph.

### Common Types of Links

#### Link Text Considerations

##### Link Text by Itself

For link text that is by itself or stands alone on its own, the text should describe the purpose of the link or provide some indication of the content of the target page.

##### Link Text within Context

The link itself combined with its enclosing text should describe the purpose of the link.

##### Images as Links

If a link contains only an image, the image's alternative text should describe the purpose of the link. If the image is paired with text inside the `<a>` element, and the text adequately describes the purpose of the link, then the image should be ignored by assistive technologies by using an empty, or null, alt attribute (`alt=""`) or by rendering it as a CSS background image.

##### Icons as Links

For icon fonts used as links, the purpose of the link should be conveyed using one of the following ARIA attributes: aria-label, aria-labelledby, or aria-describedby. The id references used for aria-labelledby and aria-describedby should properly describe the link.

## Testing Methodology

If you're not an assistive technology user, you may be tempted to just look for all of the links on the web page to determine if links are meaningful and accurately convey their purpose. While this can be done, it is important not to forget to use assistive technologies as well, as link purpose may be conveyed through text alternatives, clipped text, or ARIA attributes. Additionally, some screen readers may allow you to generate a list of all the links on the web page, which will make it easier to evaluate links out of context to see if they make sense.

### Desktop Web

When testing for the quality of link text (using a screen reader):

- Open the web browser using a screen reader and its compatible browser (e.g., VoiceOver and Safari).
- Either tab to each link on the web page to note how a screen reader renders the link, or — depending on the screen reader — generate a list of all the links on the web page.
  - For NVDA and JAWS, use the keystroke Insert + F7
  - For VoiceOver, use the Rotor to locate the list of links. The keystroke to open the Rotor is Control + Option + U, and use the arrow keys to find the list of links on the web page.
- Follow the link to visit the target page.
- After visiting the target page, determine if the link text accurately conveys its purpose, based on the page where the link takes the user, either from the link text itself (if the link is by itself) or from its context (if it is within a statement or paragraph).

### Mobile Web

#### Using Talkback and Firefox:

- You can either enable "Explore by Touch" (recommended) or use gestures to read and interact with the web page.
- If you use Explore by Touch, you can move your finger around the screen and the screen reader will render the content under your finger.
- For gestures, swipe right on the web page to read the next item on the web page. Double tap to activate a link.
- Determine if the link is appropriate either by itself or in context, based on where it takes users.

#### Using VoiceOver iOS and Safari:

- Once you are on the web page, launch the Rotor by placing two fingers on the screen and moving them in a circular motion.
- Use left or right swipes to find the list of links on the web page.
- Use up or down swipes to select a link from the list.
- Determine if the link is appropriate either by itself or in context, based on where it takes users.
