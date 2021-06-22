# The Definition Role

## Overview

The definition role is not particularly common, and screen reader support is not yet robust for this role, but when supported, it can mark a section of text as a definition. Note that HTML already provides a definition list `<dl>` structure which has better screen reader support than the definition role, so it would be better to use a definition list rather than ARIA.

### Example

```html

<p>A Footnote<sup><a href="#note-solipsism">[2]</a></sup></p>

<ol>   
  <li id="note-anomie">
    <span role="definition">
      <strong>Anomie:</strong> 
      social instability resulting from a breakdown of standards and values
    </span>
  </li>
  <li id="note-solipsism">
    <span role="definition">
      <strong>Solipsism:</strong><br>
      A) a theory in philosophy that your own existence is the only 
      thing that is real or that can be known, or<br>
      B) extreme egocentrism
    </span>
 </li> 
</ol>
```

#### Note

The role="definition" attribute should NOT be applied directly to an element that already has semantic meaning, such as the list items (<li>), because that would override the semantic meaning of the list items, which we don't want to do. We want to leave the list semantics intact.

## Example with HTML5 element dl (Definition List)

You do not need to add role="definition" to a definition list, because the semantics are already understood by the HTML markup, but the ARIA is added here to expose how definition lists are structured, from an ARIA perspective.

```html
<dl>
    <dt id="anomie-dt">anomie</dt>
    <dd id="anomie-dd" role="definition" aria-labelledby="anomie-dt">
        social instability resulting from a breakdown of standards and values
    </dd>
    <dt id="solipsism-dt">solipsism</dt>
    <dd id="solipsism-dd" role="definition" aria-labelledby="solipsism-dt">
        A) a theory in philosophy that your own existence is the only
        thing that is real or that can be known, or<br>
        B) extreme egocentrism
    </dd>
</dl>
```

## Related links

- [Official W3C documentation about the definition role](https://www.w3.org/WAI/PF/aria/roles#definition)

