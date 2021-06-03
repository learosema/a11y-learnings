# Heading Level 1 Best Practices

## The beginning of the main content SHOULD start with `<h1>`.

Usually the best practice is to start the main content of a web page with a level 1 heading (`<h1>`), with no other headings before this high-level heading. The sub-sections of the page should each be marked as level 2 headings (`<h2>`). If there are sub-sections within the level 2 sections, they should be marked as level 3 (`<h3>`) and so on. Anything that comes before the main content of the page probably should not be marked up with any headings at all, though this is not an iron-clad rule. One of the main reasons that the `<h1>` should appear at the beginning of the main content is because screen reader users can use keyboard shortcuts to navigate directly to the first `<h1>`, which, in principle, should allow them to jump directly to the main content of the web page. If there is no `<h1>`, or if the `<h1>` appears somewhere other than at the start of the main content, screen reader users will have to listen to more of the web page to understand its structure, wasting valuable time.

As with all best practice recommendations, there will be exceptions, in which it doesn't make sense to start the content with `<h1>`, or when it may be best to put other headings before the start of the main content, but the exceptions do not apply to the vast majority of web pages.

## Most web pages SHOULD have only one `<h1>`.

With few exceptions, most web pages should have only one heading level 1, to make it clear where the beginning of the main content is.

A common exception to this best practice is when a page has a modal or overlay. The modal/overlay is an element displayed on top of the main page, and the heading level of the modal title is often marked as an `<h1>`. This should not cause users confusion, however, because the modal and its heading should not be available while a user is interacting with the main page, and the main page should not be available while a user is interacting with the modal/overlay.

Another possible exception includes index pages of several blog articles combined on the same page, in which each blog article on the page starts with `<h1>`. Even this example doesn't have to be an exception to the rule though. The top heading level 1 could be the title of the blog (e.g. "Paul's camera tips"), and each blog article on the index page could start with `<h2>`. But if the individual blog articles also appear on pages of their own, those pages should start with `<h1>` and not `<h2>`, so realistically it may make more practical sense to use `<h1>` on both the individual blog article page and on the combined index page with multiple articles. It is easier to maintain the markup that way, even if it is less than ideal for accessibility.