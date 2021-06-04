# Semantic Markup for Tabular Data

## Tabular data SHOULD be represented in a `<table>`.

Screen reader users are able to navigate data tables from cell to cell, in a multi-directional way (up, down, right, left), much like navigating a spreadsheet. As they move from cell to cell, screen readers will read the associated header labels (if the table has been created with accessibility in mind). This structure and easy navigation ability with screen readers make tables well-suited to tabular data.

## Don't create fake tables

There is a downside to using tables: they don't always display particularly well on mobile devices. This downside has led developers to seek alternative ways of representing tabular data. 

One thing that many of those techniques have in common is that they use `<div>` elements and CSS to re-create the look of tables, without the appropriate underlying semantic structure.

The problem with this idea is that it breaks the ability of screen readers to communicate the semantic meaning and structure to blind users.

It also breaks the ability to navigate table cells in a multi-directional way. With the semantics and the navigation both broken, users can only proceed through the fake table sequentially — in the order the elements appear in the DOM — which is a much less effective way of exploring tabular data.

There are many techniques for making tables work better on mobile devices, few of which are ideal. As you evaluate the different approaches, if possible, choose a technique that maintains the semantic data structure of a real table, at least in the desktop view. 

Sometimes it is necessary to switch to another format (e.g. a list with labels) in the mobile view.
