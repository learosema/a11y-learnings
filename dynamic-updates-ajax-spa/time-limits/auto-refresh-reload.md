# Auto Refresh/Reload

## The page MUST NOT refresh or reload automatically.

The most common offenders of this rule are news web sites. There are legitimate reasons to want to keep the content fresh, but there are serious accessibility and usability problems with auto-refreshing pages.

Pages that auto-refresh without the user's permission cause problems for everybody. If a person is in the middle of reading the page, the screen will go blank momentarily while the page reloads, then it may take a few seconds to return.

In a best-case scenario, the visual viewport and the keyboard focus will both return to the same location. That's still annoying and disorienting, especially for users with attention deficits or cognitive disabilities.

In a worst-case scenario, the page changes significantly, and the original content is no longer there at all, or perhaps is in a different location.

Screen reader users are particularly hard-hit by auto page refreshes. It can take a long time for people to find their previous location, and then the page may refresh again.

It can be quite frustrating. In some cases, users may not have sufficient time to find their place before the page refreshes again. This is especially true for users with motor disabilities whose movements may be slow.

## A web page MAY notify the user when a refresh is recommended.

If having fresh content is critical to a web site, one way to meet that need without ruining the user experience is to provide a notification that there is newer content available.

If the update is urgent, use a dialog, or similar to notify the user. Send the focus to the dialog to ensure good keyboard accessibility, and allow users to choose to refresh the page or to return without refreshing the page.

If the update is not urgent, consider less intrusive methods of notifying users, such as an ARIA alert message that is visible on the screen and announced by screen readers, but that does NOT steal the keyboard focus.

### Example 

- [ARIA alert example](https://dequeuniversity.com/assets/html/module-dynamic/reload/good/index.html?version=1)

#### Note about keyboard focus:

The buttons to "Remind me in 5 seconds" and to "Cancel" both cause their own container (<div role="alert">) to disappear, which means that the keyboard focus will be lost unless you send it somewhere specific.

You must send the focus somewhere after these buttons are pushed. In this case, the script sends the focus to the first <h1> on the page when either of those buttons is pushed.

#### Note about emptying the alert container:

If the same alert container (or aria-live container) is going to be re-used for multiple announcements, it is always best to empty the container before writing new content to it.

Otherwise there is a risk that screen readers will not read the new content, especially if it is identical to the previous content, as it is in this case.