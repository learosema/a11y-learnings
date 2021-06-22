# Summary

## Dynamic Content

Silence is bad. When screen reader users activate a feature (link, button, control, etc.), or when an important part of the content changes, they need to hear feedback. One of the basic challenges with dynamic content is to figure out the best way to tell screen reader users about the dynamic changes. The three main options are:

- Load or reload the page, with the page `<title>` reflecting the updated dynamic information.
- Move the focus to the updated content or to a confirmation or error message.
- Use an ARIA live region to make an announcement.

## Time limits

Make sure to give users enough time to complete tasks, or to warn them when their time is about to expire, preferably giving them the option to extend their time. Don't automatically refresh or reload the page.

## AJAX

Inform users (generally by moving the focus or using ARIA live regions) when new content is loaded at the user's request (such as clicking on a link or button). 

But be careful to not announce too frequently, as in the case of lazy loading, and be sure to construct the UX in a way that allows keyboard users to reach all parts of the page (be careful with infinite scrolling).