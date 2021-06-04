# Navigation Lists

## A navigation list SHOULD be designated with the <nav> element or role="navigation".

The main navigation list(s) of a web design — such as the main navigation menu — should be marked as navigation landmarks so that screen reader users can easily find them when they pull up the list of landmarks.

It is not necessary, or even desirable, to mark every set of links as a navigation landmark. The landmark should be reserved for the most important navigation regions on the page, so that the list of landmarks does not get too cluttered.

### Good example

Use a `<nav>` element

```html
<nav>
  <ul>
    <li><a href="home/">Home</a></li>
    <li><a href="home/">Products</a></li>
    <li><a href="home/">Services</a></li>
  </ul>
</nav>
```

## A navigation list SHOULD include a visible method of informing users which page within the navigation list is the currently active/visible page.

```html
<li class="current-page">Dairy</li>
```

## A navigation list SHOULD include a method of informing blind users which page within the navigation list is the currently active/visible page.

Unfortunately, there is no official HTML or ARIA attribute that can be used to designate the current page within a navigation list (though there is talk of creating one for the next version of ARIA), so we have to resort to techniques such as:

- Visually hidden text
- aria-label
- aria-labelledby
- aria-describedby

### Good Example: Hidden Text

```html
<li class="current-page">
  <span class="visually-hidden">Current page: </span>Dairy
</li>
```

### Good example: aria-label

```html
<li class="current-page">
  <a href="#dairy" aria-label="Current page: Dairy">
    Dairy
  </a>
</li>
```
