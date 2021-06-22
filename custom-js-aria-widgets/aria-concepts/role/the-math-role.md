# The Math Role

## Overview

The topic of math on the web and MathML can get quite complicated very quickly. This section will not attempt to address all of the issues related to math accessibility, but it will show how the ARIA role="math" fits into math expressions on the web.

### Example

Note that there is an aria-label applied to the entire object, with the equation written out in words as a backup method for conveying the content within the MathML markup for screen readers and/or browsers that don't support MathML.

```html
<div role="math" aria-label="a cubed plus b squared plus c">
    <math xmlns="http://www.w3.org/1998/Math/MathML">
        <mrow>
            <msup>
                <mi>a</mi>
                <mn>3</mn>
            </msup>
            <mo>+</mo> 
           <msup>
                <mi>b</mi>
                <mn>2</mn>
            </msup> 
           <mo>+</mo>
            <mi>c</mi>
        </mrow>
    </math>
</div>
```

## Support for MathML

In general, screen reader support for math is still not as robust as it could be, but it is improving. VoiceOver on iOS supports native MathML quite well, and even allows screen reader users to navigate through the different parts of the equation; it reads both the aria-label text and the math equation itself.

VoiceOver on macOS (and OS X) also reads MathML well, but does not appear to allow users to navigate through equations as easily; it does not read the aria-label text. Neither JAWS nor NVDA support native MathML as written above.

Utilities such as [MathJax](https://mathjax.org) can improve rendering of MathML across browsers, though care must still be taken to render it in a way that works for screen readers.

## Related Links

- [Official W3C documentation about the math role](https://www.w3.org/WAI/PF/aria/roles#math)
