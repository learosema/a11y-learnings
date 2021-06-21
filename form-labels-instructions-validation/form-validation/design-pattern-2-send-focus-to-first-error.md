# Design Pattern 2: Send Focus to First Error

## Overview

Another way form validation results can help users fix errors is to send the focus to the first field that contains errors after submission. With this method, user would not have to hunt down the first error and they can navigate the form from that first error to correct other errors in the form.

## Implementation Details

Note: Many of these are similar or identical to the implementation details for Design Pattern 1: Error/Success Summary.

- Set invalid fields to aria-invalid="true".
- Move focus to the first field with an error.
- Ensure error messages are associated with form fields using aria-describedby so that screen reader users know how to fix the problem.
- Ensure error messages are visible so that sighted users know how to fix the problems. In this particular example, an error icon is visible at all times, but the error explanation is visible only when the user focuses on the field with an error or hovers the mouse over it. A tooltip message pops up with the error explanation. Advantage: Cleaner interface. Disadvantage: Users will not know how to correct the error at one glance (but they will know after focusing or hovering on the input).
- Ensure error messages are adjacent to the inputs so that screen magnification users can easily see which messages belong to which fields. In this example, the icon is directly to the left of the input. The tooltip appears directly to the right. Positioning the tooltip below the input or near the icon would probably be more effective for screen magnifier users, especially on small screens, but this layout can still be acceptable on full size screens. The styles in this example are set up so that the tooltips appear below the input on screens with smaller resolution, or when users zoom in the browser.

## If the form submission causes a new page to load (or the same page to reload):

- Ensure the page `<title>` reflects the error or success confirmation status. The title could say something like, "There were 3 errors in the form" or "Success! Your account has been created." The page `<title>` is the first thing screen reader users hear when the page loads, so it is the fastest way to give them feedback on the form submission status.
- Move the focus to the confirmation message after the page loads.

IMPORTANT: You will need to let the page finish loading, then set a JavaScript timeout of 1 to 2 seconds to allow the screen reader virtual buffer to process the page, then use JavaScript to send the focus to the confirmation message. If you send the focus to the message immediately upon page load, the focus may be set successfully, but screen readers will say nothing because they haven't had time to determine what is on the page.
