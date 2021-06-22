# Role

## Introduction:

Every HTML element has a role, meaning a set of features, properties, and methods of conveying information to and/or from the user. Essentially the role defines what the element is. Screen readers and other assistive technologies need to know the role of each element on the web page to be able to interact with it intelligently, and they need to be able to communicate the role to the user.

When a screen reader comes to an `<img>` element, for example, the screen reader knows it is an image — that the role is defined as "image" — so the screen reader will tell the user that it is an image (most screen readers say "graphic") and then it will read the alt text for the image, or perhaps read the file name or link destination if the image is missing alt text.

A screen reader will behave quite differently when it encounters a `<p>` element (where the role is defined as "paragraph").

## In this Section:

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
