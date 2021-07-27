# ARIA Concepts

## Introduction:

Before attempting to create custom ARIA JavaScript widgets, it helps to know what ARIA is and what the expected design patterns are. There are expectations in terms of keyboard interaction as well as in what kinds of information must be programmatically available to screen readers to make the widgets accessible to people who are blind. This section explains the foundation upon which all custom ARIA JavaScript widgets are built.

## ARIA Axioms:

- NEVER use ARIA unless you have to.
- ALWAYS use ARIA when you have to.
- You're doing it wrong (probably).
- This is somewhat tongue-in-cheek, but it makes some important points.

When developers first learn about ARIA, they sometimes think it can and should be applied everywhere, and that everything should now be a custom ARIA widget.

No, no it shouldn't. Use native HTML elements whenever possible. They work. People know how to use them. They're accessible. Only create a custom ARIA/JavaScript widget if there is a compelling reason to do so.

If you have a compelling reason to create a custom ARIA/JavaScript widget, use ARIA, and use it well.
ARIA is not just a matter of throwing in a few attributes here and there. It's a whole different model of user interface markup.

You have to think through the non-visual aspects of the interface. You have to learn the ARIA way of thinking, and you have to get the technical details right. The first time you try, you will probably overlook something, or many things, because you probably don't yet fully understand the reasoning behind it or the consequences of doing it wrong.

But you can learn. This section will explain the core concepts, to give you a solid foundation in the logic and patterns in ARIA techniques.

## In this Section:

- [Overview](overview.md)
- [Name](name.md)
- [Role](role)
  - Landmark Roles
  - Widget Roles
  - Pseudo HTML Roles
  - The Document Role
  - The Application Role
  - The Presentation Role
  - The Math Role
  - The Definition Role
  - The Note Role
  - The Directory Role
  - Abstract Roles
- [Value](value.md)
- [Description](descriptions.md)
- [Live Regions](live-regions.md)
- [Keyboard Accessibility](keyboard-accessibility)
  - ARIA Keyboard Patterns
  - Operability
  - Visible Focus Indicator
  - Tab/Reading Order
  - No Keyboard Trap
  - Using tabindex Correctly
  - Focus Management
  - Keyboard Instructions
