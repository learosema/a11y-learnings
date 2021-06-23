# Summary

Creating accessible custom JavaScript widgets can be tricky. There are lots of little things to pay attention to, including keyboard interaction, touch interaction, ARIA authoring practices, and even the question of whether a custom JavaScript widget is the right approach in the first place.

It's always best to start with the assumption that native HTML widgets are the best approach. They are natively accessible, and people are more used to them. They don't have to learn how to use them in the same way they have to learn how to use a custom control they've never encountered before.

Study the [WAI-ARIA Authoring Practices](https://www.w3.org/TR/wai-aria-practices-1.1/). Whenever you start on the path of creating a custom widget, find an ARIA widget that already accomplishes your goals. If there isn't one quite like what you want, first ask if what you want is really necessary, because it will be unfamiliar to users.

If you decide it is necessary, identify the closest ARIA widget match, and use those ARIA roles and design patterns as the basis for your design. It's okay to make compound widgets consisting of design patterns from 2 or more ARIA widgets, as long as the end result is intuitive to use and all of the names, roles, and properties are communicated properly to screen reader users.