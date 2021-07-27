# Notifying Users of Changes

## Introduction:

One of the biggest accessibility concerns with dynamic content is the need to notify users that the content has changed. Sighted users benefit from highlighting or drawing visual attention to the changes.

Users who are blind need to be notified some other way, such as by loading a new page, sending the focus to the new content, or using ARIA live announcements. No matter how fancy the dynamic processes get, this fundamental need to notify users of the changes remains constant.

One of the worst things that can happen with dynamic content is that screen reader users activate a feature (like clicking on a button) and they hear absolutely nothing. That's very common in modern AJAX-driven web sites, unfortunately, because developers fail to take into account the screen reader user experience.

## In this Section:

- [Option 1: Load/Reload Page](option-1-re-load-page.md)
- [Option 2: Move the Focus](option-2-move-the-focus.md)
- [Option 3: ARIA Live](option-3-aria-live.md)
- [Status Messages](status-messages.md)
