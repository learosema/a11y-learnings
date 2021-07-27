# Why Test with Screen Readers?

## People need screen reader access

The most important reason to test with screen readers is because real people need screen reader access. Don't lose sight of that goal. Screen reader accessibility is a technical requirement, but we're doing it to benefit human beings who rely on us to do our job as developers, designers, and testers so they can access their computers.

## Automated accessibility tools can't catch every accessibility issue

Automated accessibility tools can find a lot of accessibility issues in web content, such as images missing alt text, form input elements missing labels, and many more. Automated accessibility tools are a valuable part of the overall accessibility development and QA workflow.

Even so, automated tools cannot find all the potential accessibility problems. There are certain types of issues that are difficult for automated tools to identify, such as:

### Quality and accuracy

Inaccurate or poor-quality alt text is no better than missing alt text. Automated tools can only tell you whether an image has alt text. They cannot tell you whether the alt text is accurate or meaningful. The same is true of text labels for form elements, captions on tables, headers on data tables, and so on.

### Keyboard focus patterns

Automated tools cannot reliably determine where the keyboard focus should be at any given point in time. When a user clicks on a button, the focus should go to a logical destination—such as a dialog or error message—but it is impossible for an automated tool to know what the appropriate focus location is.

### Custom widgets

With custom widgets, like dialogs, carousels, and accordion menus, there is no way for an automated tool to detect all the possible ways of creating them incorrectly, especially when it comes to keyboard interaction patterns. At best, an automated tool might be able to identify when a widget is created correctly, by comparing the names, roles, values, and keyboard focus patterns of the widget with the ARIA 1.1 authoring practices opens in a new window document. Even that is tricky.

It is difficult to estimate the percentage of accessibility issues that automated tools can find—especially because every web site is different—but the range of the estimate is usually between 30% and 50%. The more complex the web site in terms of scripting and custom widgets, the lower the estimate would be. Automated tools have their place, but you can't rely on them to do all your work for you.

## Custom widgets with JavaScript and ARIA require screen reader testing

The only way to know if a custom widget works with a screen reader is to test it with a screen reader. This is especially true when trying to implement ARIA widgets according to the ARIA 1.1 authoring practices opens in a new window. A badly implemented ARIA widget can be a disaster for accessibility. Even though the whole purpose of ARIA is to make things more accessible, there is enough power in ARIA to break accessibility completely when used inappropriately. That would be a bit extreme, but still, flaws in your ARIA techniques are best discovered by testing with a screen reader.

## Screen reader brands aren't exactly alike

When testing static HTML accessibility—things like paragraphs, lists, headings, landmarks, and images—it is usually enough to test in only one screen reader, and it doesn't matter which screen reader you choose. They all are capable of rendering that type of content. They sometimes render it differently, but those are stylistic differences that don't matter much.

When testing dynamic content—like custom JavaScript widgets and form validation—it is important to test with at least two screen readers, because there can be subtle differences in the way they handle the dynamic content. Sometimes there are even dramatic differences, or bugs in one of the screen readers, which can be important to take into account. Usually the differences are a matter of support for a given ARIA attribute or method, as opposed to outright bugs, but bugs do exist.

The support for ARIA across screen readers is quite good, but it is still evolving. None of the screen readers supports 100% of the ARIA specification, unfortunately, but they do come relatively close.
