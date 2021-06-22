# The Note Role

## Overview

The note role is similar in concept to the HTML 5 `<aside>` or the ARIA `role="complementary"`, but `role="note"` is not a landmark region like the other two and is generally meant to be read in the context of the rest of the content around it. Also, <aside> and role="complementary" should make some sense on their own. The same is not necessarily assumed of `role="note"`.

## Example

```html
<p>There are ways to safely view a solar eclipse, including using welder's goggles 
rated at 14 or higher, or looking at the projected image of a pinhole camera.</p>

<p role="note"><strong>Important:</strong> Never look directly at the sun with 
your bare eyes, or through a camera, or through binoculars.</p>
```

## Related links

- [Official W3C documentation about the note role](https://www.w3.org/WAI/PF/aria/roles#note)