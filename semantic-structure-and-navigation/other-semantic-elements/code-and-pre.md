# `<code>`, `<pre>`

## Code SHOULD be marked with the `<code>` element and styled to look different from non-code text.

Sighted users benefit from being able to tell, via visual styling, when code is used, so they can tell the difference between technical terms and regular prose. The default styling for the `<code>` element is a monospaced font, often Courier or Courier New.

## Screen Readers and the code Element

Screen readers don't support the `<code>` element. In principle, blind users could also benefit from knowing the difference between code and prose, but screen readers ignore the `<code>` element completely. 

So even though the `<code>` element is semantically correct, screen reader users don't benefit from it, at least with current screen readers.

## Blocks of code SHOULD be formatted with the `<pre>` element.

Using the `<pre>` element around blocks of code helps sighted users distinguish the code from the surrounding text. 

The text will be preformatted exactly as it appears in the source code, including spaces (HTML allows only one space in normal markup). 

The `<pre>` element is just for visual formatting, so it is not semantically meaningful. If the preformatted text contains code, it is appropriate to wrap the inner text in a `<code>` element.