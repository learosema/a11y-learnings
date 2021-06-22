# Lazy Loading

## Overview

"Lazy loading" AJAX content is content that loads almost at the same time as the rest of the page, but there is a slight delay, due to things like server-side script delays, complex database queries, time-consuming authentication steps, or anything else that might slow down a web page. The main page is designed to load quickly, and the rest of the page is supposed to load shortly thereafter. The developers separate the two load events (main page versus AJAX parts) to give end users a better overall experience.

Lazy loading is a legitimate design approach with almost no impact on accessibility. Problems can arise, though, under two circumstances:

If the user arrives at the blank spot where the content has not loaded yet.
If the developers get too carried away with ARIA live messages that they think will benefit screen reader users, when they actually make things worse by overwhelming them with non-essential "content loaded" messages.

## Placeholders for AJAX content SHOULD inform screen reader users that the content is loading.

If users arrive where content has not yet loaded, it's best to have a placeholder there. For sighted users, this can consist of a "spinning wheel" icon, or a progress bar animation, or an hourglass animation, or a "Please wait" message of some sort. Screen reader users also need to know that content will load in that area.

### Example

```html
<img src="spinning.gif" alt="Content loading" width="36" height="36">
```

## "Lazy loading" AJAX content SHOULD NOT be announced as it loads.

The assumption with lazy loading content is that it will load quickly enough that it will have no impact on screen reader users. If there is a reason to believe that the content will load slowly then an ARIA live announcement may be appropriate, but if the content is designed to load relatively quickly, it's best to make no announcement at all.

- [Bad example: too many aria-live announcements](https://dequeuniversity.com/assets/html/module-dynamic/lazy-loading/bad/index.html)
- [Good example: lazy loading with no interruptions](https://dequeuniversity.com/assets/html/module-dynamic/lazy-loading/good/index.html)

