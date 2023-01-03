# Quality Management

## Writing QA Tests During the Planning Phase

One of the jobs of the QA team is to write tests based on the requirements written in the early planning phase. The clearer the accessibility requirements, the clearer the tests will be, the greater the chance that the testing team will catch all of the important accessibility bugs.

## User Stories

User stories can be written into the design requirements. As an organization gets more mature in its accessibility efforts, many of these user stories can be recycled from one project to the next, because the accessibility needs remain constant, even though the implementation details vary from one design to the next.

You should write user stories for various kinds of disabilities. Here are a couple of examples.

### User Story Example: Blind User; Labels on Form Input Fields

```
AS a blind screen reader user using the tab key to navigate the form fields,
I WANT my screen reader to read the label of a form input
SO THAT I know what the form input is for.
```

### User Story Example: Low Vision User; Good Contrast on Text

```
AS a low vision user who has difficulty seeing low contrast text,
I WANT to be able to clearly distinguish the text from the background (with a contrast ratio that passes WCAG AA guidelines)
SO THAT I can read the text.
```

## Acceptance Criteria

Developers need to have clear guidance to know when they have succeeded in meeting the design goal. To continue with the previous examples, we could say create the following acceptance criteria:

### Acceptance Criteria Example: Blind User; Labels on Form Input Fields

The form input has programmatically determinable text using one of the following methods:

- Explicit label (`<label for="name">Name:</label> <input id="name" type="text">`)
- Implicit label (`<label>Name: <input type="text"></label>`)
- `aria-label` or `aria-labelledby` (only under conditions where explicit or implicit labels won't work

### Acceptance Criteria Example: Low Vision user; Good Contrast on Text

The text passes the WCAG AA guidelines for color contrast as determined by running the aXe browser extension on the content.

## High Quality Bug Reports

The QA team needs to learn how to write very specific bug reports that explain the accessibility defects in ways that make sense to developers who may not be accessibility experts themselves.

## Testing by Users with Disabilities

One of the most valuable things you can do for quality assurance is have people with real disabilities test your web content. Hire some blind QA talent who are expert screen reader users, or people with low vision, or people with other kinds of disabilities.

They'll tell you whether you've succeeded or not, and their very presence as a member of your team will help to transform the outlook of the entire team. No longer will accessibility be a vague abstract concept. They'll understand it at a deeper level, because they'll be able to observe and interact with a peer with a disability.
