# Giving Users Keyboard Instructions

## When custom keyboard behavior is required to use a component, keyboard instructions MUST be provided.

What if your JavaScript widgets are 100% keyboard-accessible, but people don't know how to use them? You could say, "I did my part. They will figure it out." But there are so many possible ways of creating common interactive widgets that it can be frustrating for the user if they don't know what interaction pattern you're using. 

Or, maybe you have created a new, one-of-a-kind, bleeding-edge, custom widget that no one has interacted with before. You've taken pains to make sure all of the interactions can be done by keyboard in addition to the mouse; let your users know it!

Keep in mind that there are two main audiences with keyboard accessibility:

- Sighted keyboard users
- Blind screen reader users

There is a tendency for developers to forget sighted keyboard users, so make sure you don't do that. Keep the message brief. It could say things like: "Tab to the XXX, use your up and down arrow keys to YYY and left and right arrow keys to ZZZ."

Here are some possible ways to provide keyboard instructions:

- Write the instructions above the widget for everyone to see.
- Make the instructions appear as a pop-up tooltip when the widget receives focus. Use aria-live to announce the text in the tooltip for screen readers.
- Make the instructions appear as normal text when the widget receives the focus. Consider adding an outline or background color to draw attention to the text for sighted users. Use aria-live to announce the text for screen readers.

You may be able to come up with other ways to instruct the user of the keyboard pattern. Just be sure that your methods work for both sighted keyboard users and blind screen reader users.

## ARIA widgets that require more than just the Tab key to interact with may be confusing to users, so you MAY provide keyboard instructions.

Even when ARIA widgets follow the ARIA authoring practice recommendations, users may be unfamiliar with the ARIA recommendations and may expect to use the tab key to navigate everywhere in a website. 

You may want to consider giving keyboard users some prompts to let them know how to interact with your ARIA widgets such as tree views, tab panels, and datepickers. (See the page on "The ARIA Keyboard Interaction Module" for a deeper discussion on ARIA widget keyboard patterns.)

### Note:

As both users and developers get more familiar with the ARIA keyboard interaction patterns, the use case for providing instructions for standard ARIA interactions will decrease.