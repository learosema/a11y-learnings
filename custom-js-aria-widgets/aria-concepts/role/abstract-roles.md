# Abstract roles

## Overview

The final type of ARIA role is the abstract role. You can't use any abstract roles in your code, so they're not useful at all in a practical sense. They're included here just for the sake of completeness, because they're defined in the specification. Think of them as categories of roles, rather than as actual roles themselves. As defined in the spec, abstract roles include:

- `command`
- `composite`
- `input`
- `landmark`
- `range`
- `section`
- `sectionhead`
- `select`
- `structure`
- `widget`

### Note:

You can't actually use any of the abstract roles directly in your document. For example, role="widget" would NOT be valid to write in your code. Some things are understood to be widgets, but you can't specify a widget yourself. Browsers do that for you.

## Related Links
- [Official W3C documentation about abstract roles](https://www.w3.org/WAI/PF/aria/roles#abstract_roles)
