# Option 1: Load or Reload Page

## Overview

One of the easiest ways to alert people to new content is to send them to a new page or to reload the current page. This is the oldest method and requires no JavaScript. You simply have the user activate a link.

When a new page is loaded or when the same page is reloaded, most screen readers do the following:

- Read the page title
- Provide a summary of features on the page (such as "7 headings, 3 regions, and 27 links")
- Start reading from the top of the page

When these events begin to happen, screen reader users know they are on a new page (or that the current page is reloaded, if they hear the same title as the page they were just on), so they expect that they are about to hear some new content.

## Accessibility Considerations

There is nothing inherently inaccessible about loading a new page (unless it occurs unexpectedly), but there are a couple of considerations worth noting:

### Ensure the page title accurately reflects the content of the page AND the result of any user actions. 

For example, if the user just submitted a form with errors, the page title needs to reflect the error state. It could say something like, "Error: please correct 3 errors in the form."

### Make it easy to navigate to the main content.

If the new content is buried somewhere in the middle of the web page, it might be hard to find. Screen reader users and sighted keyboard users must skip past all of the content in the header and navigation to arrive at the main content.

If the page uses headings and landmarks, this is rather easy for a screen reader user to do, because there are keystrokes designed for that purpose. Sighted keyboard users don't have those keystrokes available, so a "skip to main content" link is recommended. Be sure the destination of that link has tabindex="-1", or else it won't work in some browsers.