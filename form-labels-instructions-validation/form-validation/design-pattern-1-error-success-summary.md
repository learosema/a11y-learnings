# Design Pattern 1: Error/Success Summary

## Overview

One way you can provide users with feedback upon form submission is to display a summary at the top with the message (either a success message or a failure message).

## Implementation Details

- Set invalid fields to aria-invalid="true"
- Move focus to error/success message
- Ensure error/success message container is set to tabindex="-1". Otherwise, focus cannot be set successfully.
- Provide a count of errors so that users get a sense of the scope of the problem.
- Ensure error messages are associated with form fields using aria-describedby so that screen reader users know how to fix the problem
- Ensure error messages are visible so that sighted users know how to fix the problems
- Ensure error messages are adjacent to the inputs so that screen magnification users can easily see which messages belong to which fields.

### If the form submission causes a new page to load (or the same page to reload):

- Ensure the page `<title>` reflects the error or success confirmation status. The title could say something like, "There were 3 errors in the form" or "Success! Your account has been created." The page `<title>` is the first thing screen reader users hear when the page loads, so it is the fastest way to give them feedback on the form submission status.
- Provide a quick way to reach the status message. Some options include:
  - Provide a "skip to main content" link that takes the users to the message.
  - Move the focus to the confirmation message after the page loads.

IMPORTANT: You will need to let the page finish loading, then set a JavaScript timeout of 1 to 2 seconds to allow the screen reader virtual buffer to process the page, then use JavaScript to send the focus to the confirmation message. If you send the focus to the message immediately upon page load, the focus may be set successfully, but screen readers will say nothing because they haven't had time to determine what is on the page.