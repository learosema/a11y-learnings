# Ineffective Designs

## Overview

- Some a11y designs start out as bad ideas even before they're built. 
- A11y is common sense to some extense, but requires more expertise in other ways.
- Involve a11y experts from start and in the design phase (and all phases), otherwise a11y is going to fail

- Not everyone needs to be a web a11y expert (but the more the better)
- ideal if all team members have basic a11y knowledge
- so the a11y experts can focus on trickier challenges of highly interactive content


## Designs that fail to take best practices in account

- most a11y failures seem like obvious failures of common sense
- common sense is not as common as we would like it to be :(

### Bad example

- Steep wheelchair ramps: when to steep, they're not useful and even dangerous (a wheelchair user is likely to crash, or needs assistance)

### Ineffective designs on the web

It's easy to ignore the guidelines and regulations about web a11y, or to take shortcuts or implement them only partly or poorly.

Poorly designed solutions don't solve a11y challenges. It's worth to do it right.

Which guidelines? Mainly the [WCAG 2.1](https://www.w3.org/TR/WCAG21/)

- no semantic markup: if there's no semantic document structure (headings, landmark roles), it's hard for screenreader users to navigate through the content
- custom widgets without ARIA markup: The widgets will not make sense to screenreader users if they don't properly expose information about names, roles and values of components, in accordance with ARIA techniques.
- custom widgets without proper keyboard management: you have to design the keyboard interaction user experience.  When you have custom widgets that hide and show components, post announcements, involve AJAX requests, you have to keep track of where the keyboard focus is at all times, and ensure the focus responds in a logical way to user requests and to scripted events.
- Poor color contrast: you're excluding people with low vision
- Form validation with visual cues only: When there are errors after a form validation process, you have to do more than change the way things look (e.g. by putting a red outline around the fields with errors). People who are blind won't be able to see the visual changes at all.

There are many other kinds of accessibility design failures besides these, but these are common sources of accessibility errors.
