# The Presentation Role

## Overview

Marking a section as `role="presentation"` essentially cancels the native role of the element and turns it into the equivalent of a `<span>` or `<div>`, which are neutral, un-semantic tags that convey no role. This is kind of the opposite of the "pseudo HTML" roles (described on the Pseudo HTML Roles page earlier in this section), which add a semantic role to an element, even if it was just a neutral `<div>` or `<span>` to begin with.

### Note:
Adding `role="presentation"` does NOT hide the element from anyone. Sighted users will still see it, and blind users will still hear the text, but their screen readers won't announce any kind of semantic role for the text.

### Exampe

```html
<h1 role="presentation">Deep Thoughts</h1>
<!-- won't be considered as a heading -->
```

Instead of saying "Heading level 1: Deep Thoughts" as it normally would, the screen reader will simply say "Deep Thoughts."

## Related links

- [Official W3C documentation about the presentation role](https://www.w3.org/WAI/PF/aria/roles#presentation)