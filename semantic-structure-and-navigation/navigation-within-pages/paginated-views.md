# Paginated views

## A paginated view SHOULD include a visible method of informing users which view is the currently active/visible view.

## A paginated view SHOULD include a method of informing blind users which view is the currently active/visible view.

A paginated view can include things like multiple pages of search results, a long table that has been split into multiple views so that it is more manageable, etc. The paginated view may be a custom JavaScript widget that technically stays on the same page the whole time, or it could be a server-side script that loads different pages for each view, or it could be a combination of those approaches.

There is no official accessibility requirement to let users know where they currently are in a paginated view, and in fact there is no native technique to do so for screen reader users, other than to use text to indicate "you are here" or "currently selected" or similar. Sometimes users can figure out where they are based on other cues, such as the page title or the text in the `<h1>` at the beginning of the main content, but it is a better user experience if the current location can also be explicitly available to the screen reader user.

### Example

```html
<li class="current-page">
  <span class="visually-hidden">Current page: </span>
  3
</li>

<!-- or aria-label -->
<li class="current-page">
  <a href="#3" aria-label="Current page: 3">
    3
  </a>
</li>
```
