# Dynamic JavaScript

## Full Accessibility of Interactive Components

### Dynamic JavaScript

Make dynamic JavaScript accessible by marking up the name, role, state, properties of elements appropriately with ARIA (and changing them dynamically if necessary), and by controlling keyboard focus.

## ARIA: Accessible Rich Internet Applications

In the early days of the web, making dynamic content accessible to screen reader users was quite difficult, or even impossible, because there was no built-in way in HTML or JavaScript to announce dynamic changes. That all changed with the introduction of ARIA (Accessible Rich Internet Applications).

ARIA markup can be inserted in HTML to announce such things as when a tab is selected or when a checkbox is checked or when a tree view is expanded.

JavaScript programmers need to keep track of these events and implement the logic necessary to put the right markup in the right places at the right times, which means that it can sometimes take a fair amount of work and technical knowledge to use ARIA effectively, but the good news is that it works. ARIA makes it possible to make interactive JavaScript accessible to people who can't see them. ARIA allows web pages to talk to screen readers in ways that were simply impossible before.

## Controlling Keyboard Focus

Keyboard accessibility is always important, but it takes on an even greater level of importance when dealing with interactive JavaScript, because you have to program the accessibility into the interactions. Once you start playing around with JavaScript, you can do pretty much anything you want.

It's kind of a free-for-all, which is great, except for the fact that the keyboard focus will not follow the action unless you tell it to. Programmers have to be very careful to not lose track of the keyboard focus at any point in time during the interactions.

It can be somewhat of a painstaking task to plan for keyboard accessibility in complex JavaScript widgets, but it is absolutely necessary, or else keyboard users—whether blind or sighted—will not be able to use the widgets.
