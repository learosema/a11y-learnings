# Interstitial views

## Screen reader users MUST be informed when a web page launches an interstitial view, a progress indicator, or enters into a paused or busy state.

The worst thing that screen reader users can hear after activating a button is silence.

If screen reader users experience silence, they're likely to ask themselves, "Did it work?" "Did my screen reader freeze up?" "Did my browser freeze up?" "Should I refresh the page?" They need some feedback.

When the user requests an action that will take a long time to complete, such as searching for airline tickets, it is common to present an interstitial or intermediate page to users as a way to confirm that the link worked, and that the results are coming if they wait. Screen reader users need that same kind of confirmation. The following two options are usually the most appropriate:

- Move the focus to the interstitial message OR
- Announce the interstitial message via an ARIA live region

Ideally, the interstitial message will not be on the screen long, so make it a short message to ensure the screen reader can read the whole thing before the next page appears.

### Example

[Good example](https://dequeuniversity.com/assets/html/module-dynamic/interstitial/good/index.html)

- the interstitial view is an aria-live region, so it gets anounced to screen reader users
- after the loading is done and the interstitial view is removed, the focus is moved to the table header
- the screen reader reads the `caption` of the table

#### Note 1

When using ARIA live regions, be sure that the region is in the DOM on page load and that it is empty to begin with. Insert the message into the live region when appropriate.

#### Note 2

When moving focus to a container that has been loaded via AJAX, be sure to use a JavaScript timeout (generally 1 to 2 seconds) AFTER the content has loaded before sending the focus to the new container. Also, be sure that the container is set to tabindex="-1".