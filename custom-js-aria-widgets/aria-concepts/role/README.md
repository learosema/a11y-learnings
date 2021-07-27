# Role

## Introduction:

Every HTML element has a role, meaning a set of features, properties, and methods of conveying information to and/or from the user. Essentially the role defines what the element is. Screen readers and other assistive technologies need to know the role of each element on the web page to be able to interact with it intelligently, and they need to be able to communicate the role to the user.

When a screen reader comes to an `<img>` element, for example, the screen reader knows it is an image — that the role is defined as "image" — so the screen reader will tell the user that it is an image (most screen readers say "graphic") and then it will read the alt text for the image, or perhaps read the file name or link destination if the image is missing alt text.

A screen reader will behave quite differently when it encounters a `<p>` element (where the role is defined as "paragraph").

## In this Section:

- [Landmark Roles](landmark-roles.md)
- [Widget Roles](widget-roles.md)
- [Pseudo HTML Roles](pseudo-html-roles.md)
- [The Document Role](the-document-role.md)
- [The Application Role](the-application-role.md)
- [The Presentation Role](the-presentation-role.md)
- [The Math Role](the-math-role.md)
- [The Definition Role](the-definition-role.md)
- [The Note Role](the-note-role.md)
- [The Directory Role](the-directory-role.md)
- [Abstract Roles](abstract-roles.md)
