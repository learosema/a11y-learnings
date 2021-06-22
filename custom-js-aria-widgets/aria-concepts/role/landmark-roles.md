# Landmark roles

## Overview

Screen reader users can't discern the visual design of a page, so they need a non-visual way to be able to tell the navigation from the main content or the footer or other regions. ARIA landmark roles provide a way to do this. 

When you define landmark regions, screen reader users can list all regions to understand how the page is organized, then they can navigate directly to the region they're interested in. Available landmark regions include:

- application
- banner
- complementary
- contentinfo
- form
- main
- navigation
- search

### Note:

HTML 5 defines landmarks as well, with such tags as:

- `<header>` (equivalent to role="banner")
- `<nav>` (equivalent to role="navigation")
- `<main>` (equivalent to role="main")
- `<aside>` (equivalent to role="complementary")
- `<footer>` (equivalent to role="contentinfo")

You can use either ARIA landmarks or HTML 5 landmarks — or combine them, e.g. `<nav role="navigation">` — and the effect will be the same.

## Related links

- Article: [ARIA Landmark Roles](https://www.w3.org/WAI/PF/aria/roles#landmark)
- Article: [ARIA Landmarks](https://accessibility.oit.ncsu.edu/it-accessibility-at-nc-state/developers/accessibility-handbook/aria-landmarks/)
- Article: [Easy ARIA Trip #4 - Landmarks](http://www.marcozehe.de/2009/10/31/easy-aria-tip-4-landmarks/)
- Article: [Using WAI_ARIA Landmarks 2013](http://blog.paciellogroup.com/2013/02/using-wai-aria-landmarks-2013/)
- Article: [WAI-ARIA Landmark Roles Cheatsheet](http://mcdlr.com/wai-aria-cheatsheet/)