# Error Prevention

## Best practices

The goal is to design forms that are self-explanatory so that users don't make mistakes. We've already covered many techniques which help prevent errors. Here is a short list of techniques:

### Labels:

Ensure all form elements are labeled accurately and available to all users.

### Instructions:

If the label is not enough to describe the purpose of an input, provide extra instructions.

### Built-in constraints on inputs:

Where appropriate, allow only certain kinds of input, such as only numerals when typing a zip code. To restrict the options even further, pre-define them as data values in <select> lists, radio buttons, checkboxes, or some other fixed format.

### Constrained step-by-step views:

When there are diverging paths through an interaction, it's usually not a good idea to show all possibilities at the same time. It can be confusing for users, and difficult in terms of the programming logic to ensure that all possibilities and error states are taken into account. Allow users to make a choice, then show the resulting set of choices for that path only.

### Conventional design patterns:

The more familiar your users are with the methods you're using in your design, the easier it will be for them to understand what to do. This includes using traditional form inputs as much as possible and using custom widgets only when necessary.

### Visual design that focuses user attention:

Ensure labels and instructions are near their respective inputs. Reduce distractions in the visual design. Use visual cues to guide users to fill out the form properly. Make error messages and confirmation messages visually obvious.

### Confirmation prior to submitting:

Summarize what will happen when the user submits the form, BEFORE the form is submitted. Ask the user to verify that the information is correct. This is especially important when actions are irreversible.

### Confirmation after submitting:

Summarize the result on the screen after the form is submitted, to let users review their action once again.

### Reversible actions:

Whenever possible, allow users to reverse actions to restore things to their previous state. In some cases, it may be beneficial to save multiple past actions to allow users to roll back to one of several previous states. Reversible actions can be accomplished through an "undo" feature, through a way to contact customer service, or through some other method to correct mistakes.

### Email confirmation:

Where appropriate, send an email confirmation to users as an additional safety check so they can feel confident that the action worked as intended.