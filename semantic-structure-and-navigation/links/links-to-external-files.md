# Links to External Sites, New Windows, Files

## A link that opens in a new window or tab SHOULD indicate that it opens in a new window or tab.

It can be helpful to users to know when a link will open a new window. Including a text indication (e.g. "opens in a new window") or an icon with equivalent alt text are two of the most common ways to indicate this. Ensure the indication is available to both sighted users and blind screen reader users.

```html
<p>
  <a aria-describedby="a11y-message--new-window" class="icon--new-window" 
  href="https://dequeuniversity.com" target="_blank">Deque training</a>
</p>
  .
  .
<span aria-hidden="true" class="visually-hidden" id="a11y-message--new-window">(opens new window)</span>
```

`opens new window` is read by the screen reader when the link gets focused. the `aria-hidden=true` makes the text invisible in the normal text flow.

## A link to a file or destination in an alternative or non-web format SHOULD indicate the file or destination type.

It can be helpful to users to know when a link will open a file or lead to a destination in a non-web format, such as a Word document, PDF document, Photoshop document, etc. Including a text indication (e.g. "PDF document") or an icon with equivalent alt text are two of the most common ways to indicate this. Ensure the indication is available to both sighted users and blind screen reader users.

## A link to an external site MAY indicate that it leads to an external site.

It can be helpful to users to know when a link will take them away from the current web site to a different web site. Including a text indication (e.g. "link leads to an external site") or an icon with equivalent alt text are two of the most common ways to indicate this. Ensure the indication is available to both sighted users and blind screen reader users.
