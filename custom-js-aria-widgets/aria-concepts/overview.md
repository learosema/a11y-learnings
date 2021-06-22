# Overview

## What can ARIA do?

ARIA allows you to communicate the following information to screen readers:

- labels or names for items (e.g. using aria-label or aria-labelledby or similar)
- roles, role="navigation", role="main" etc.
- states of dynamic/interactive components (e.g. aria-selected="true", aria-expanded="true", aria-hidden="true")
- properties of items (e.g. aria-haspopup="true")
- relationships between items (e.g. aria-owns, aria-controls, both of which describe a kind of parent-child relationship where one item owns or controls another)
- live announcements in real-time that are passed on to screen readers

## ARIA is Useful Only to Assistive Technologies

ARIA does not change anything for sighted users. For example, aria-hidden="true" does not hide content from visual users, but it does hide it from screen reader users.

## ARIA is Not a Programming Language

ARIA has no procedural logic or interactivity on its own. To create a tree menu or a tab panel, or any other interactive widget, you need to use JavaScript to give the content functionality, and you use ARIA to label things appropriately with names, roles, states, properties, and relationships.

ARIA is essentially an API for communicating this information to screen readers.
