# Visibility of Group Labels

## Group labels SHOULD be adjacent in the DOM to the grouped elements.

When screen readers are reading a page using browse mode, they read information in the order it appears in the DOM. If group labels and their associated form fields are not adjacent to each other in the DOM, screen reader users may have trouble associating the group label and form fields as they are browsing a page.

### Bad

- visually hidden legend text, but accessible to screenreaders (make it visible for all users)
- poor text/background color contrast on legend text
