# Robust

## Defining Robustness

Robustness is about ensuring compatibility with a broad range of user agents, including assistive technologies.

Different user agents (browsers and other web devices) parse web content differently. The differences are apparent across platforms (Windows, Mac, iOS, Android, Linux, etc.), and even across different versions of the same browser.

For example, Internet Explorer 8 parses HTML quite differently from Internet Explorer 11, in part because of bug fixes and features added, and in part because of advances in support for newer web specifications, such as HTML 5 and CSS 3.

Different versions of screen readers also handle content differently, with newer versions featuring better support for newer technologies such as ARIA. It would be impossible to support all possible combinations of all user agents. There are too many to take into account, and some of them simply aren't robust enough themselves to handle the kinds of things that are necessary for ideal accessibility.

You'll have to draw a line in the sand somewhere and say that you'll support Internet Explorer only back to version X, or that you won't support browser Y because its user base is so small and/or because the browser doesn't have a feature set that is rich enough.

## Use Standard Markup

One of the best ways to increase the likelihood of robust markup and code across user agents is to use standard markup. To the extent possible, the content should be validated using appropriate validators. You can validate the HTML (see the [W3C HTML validator](https://validator.w3.org/)), CSS (see the [W3C CSS validator](https://jigsaw.w3.org/css-validator/)), JavaScript (you can use a tool such as the Chrome/Firefox Developer Tools to inspect the code, or an online tool such as [ESLint](https://eslint.org)), and other aspects of the markup.

Valid markup doesn't guarantee accessibility. And in fact, valid markup is not always necessary for accessibility; it is not a one-to-one relationship between validity and accessibility or robustness.

Even so, valid code definitely helps eliminate some of the issues that can lead to problems in different user agents, making your job easier when it comes to narrowing down the causes of potential accessibility problems.

## Use ARIA (or other means) to Indicate the Name, Role, and Value of Interactive Components

In the old days of the web, web pages were basically static. They did not have much capability for interaction. These days, most major web sites are highly dynamic, often using custom widgets and scripts to create opportunities for interaction and dynamic display of information.

This high level of interactivity demands careful attention to how objects are marked up. Screen reader users need to know that an item is expandable and whether it is currently expanded or collapsed (`aria-expanded="true"` or `aria-expanded="false"`). They need to know if a tab is selected or not (`aria-selected="true"` or `aria-selected="false"`).

It's not enough to set these properties once on a page. These properties need to be updated dynamically using JavaScript when their state changes. ARIA ("Accessible Rich Internet Applications") provides a wealth of capabilities for dynamic content that were very difficult or impossible to achieve before. Learn ARIA and apply it.

## See Also:

- The official Web Content Accessibility Guidelines, [Principle 4: Robust](http://www.w3.org/TR/WCAG20/#robust).
