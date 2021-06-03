# Creating Landmarks (HTML5, ARIA)

## Landmarks SHOULD be used to designate pre-defined parts of the layout (<header>, <nav>, <main>, <footer>, etc.).

Use either HTML 5 landmarks or their ARIA equivalents to mark sections of the layout in the design, so that screen reader users can easily find their way around the layout.

### Note:

Landmarks are used to designate sections of the overall _page design and layout_. Headings are used to designate sections _within the content_.

## HTML5 landmarks and their ARIA equivalents

The alignment of ARIA roles and HTML5 elements is not exact. The intentions and purposes are somewhat different between the two specifications, but the following table presents a reasonable interpretation of some of the ways HTML5 and ARIA can overlap.

### Note:

As a general rule, it is usually best to use native HTML elements rather than their ARIA equivalents whenever possible. That said, the end result is effectively the same for screen reader users, so either one can be used. Adding ARIA roles to existing markup can sometimes be easier to manage, because adding new HTML elements can sometimes alter the visual appearance (and require extra CSS work), whereas ARIA roles do not.

| HTML5    | ARIA role      | Listed among landmarks by most screen readers     |
|----------|----------------|---------------------------------------------------|
| header   | banner         | yes                                               |
| nav      | navigation     | yes                                               |
| n/a      | search         | yes                                               |
| main     | main           | yes                                               |
| footer   | contentinfo    | yes                                               |
| aside    | complementary  | yes                                               |
| section  | region         | mixed support (only with aria-label/labelledby)   |
| article  | article        | mixed support, JAWS yes, others not               |
| form     | form           | mixed support (ARIA role works, html5 not)        |

### Note:

The ARIA region and article roles are not considered landmarks, even though their HTML5 counterparts are.


The most useful of these for most websites are header/banner, nav/navigation, main, and footer/contentinfo. The others may be used as well, but they are not as widely applicable across most websites.
