# Progressive form updates

## Overview

Sometimes you need to collect information a step at a time, with the result of the first step determining the options available in the next step. You can make that kind of interaction accessible by following a few best practices:

### Change future options, not past options

Screen reader users experience web content more linearly than sighted users. If a screen reader user has already been to a part of the form, the user is unlikely to go backward just to check to find out if something changed. Ensure that any dynamic changes occur further down in the DOM, rather than further up in the DOM.

### Allow users to change past choices

In some cases, users may wish to go backward in the flow of the interaction. Provide an easy way to do that.

### Consider limiting access to one step at a time

Having multiple steps on the screen at the same time can be overwhelming and confusing. Sometimes it can be appropriate to leave past options visible and editable on the screen as the user moves forward.

Other times it is best to disable the choice mechanism of past options, and instead display a summary of the previous choices (as long as there is a way to edit those previous choices).

### Number the steps

Users appreciate knowing how many total steps there are in the process, and which step they are on currently.

### Manage keyboard focus

Manage the focus at every step of the way.

Depending on how the interaction is constructed, you may not always need to set the focus on the new items, but if the item currently in focus ever disappears, you will need to set the focus somewhere, preferably on the next logical step in the process, either on the next relevant form element, a relevant heading (with tabindex="-1", or on a container (with tabindex="-1").

Be sure to pay attention to both forward and backward paths through the interaction.

### Consider providing a concise summary of the choices

It can be burdensome to look back through a lengthy form or to backtrack through a step-by-step form. A concise summary can make the result easier to understand.

It may also be appropriate to programmatically associate the summary with a final "Submit" button, especially if the summary occurs prior to the button in the DOM, as shown in the code below:

```html
<div id="summary">Summary goes here ... </div>
<button aria-describedby="summary">Submit</button>
```

### Example

The example below uses a step-by-step design, with only one step visible on the screen at a time. The steps are numbered ("step 1 of 4" etc.), and the focus is managed both forward and backward (focus is set on the selected button, if applicable, or else on the first radio button in the group). A summary of the choices is shown on the screen and is programmatically associated with the final "Purchase" button, for the benefit of screen reader users.

- [Go to the progressive form example](https://dequeuniversity.com/assets/html/module-forms/progressive/good/index.html)

Note: This example could be modified to leave the past choices editable on the screen. Either way can be accessible as long as the overall process is designed according to the points outlined above.s