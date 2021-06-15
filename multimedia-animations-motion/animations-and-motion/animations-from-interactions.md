# Animations from Interactions

## A user SHOULD be able to disable motion animation triggered by interaction, unless the animation is essential to the functionality or the information being conveyed.

Some people may experience negative effects from page animations. For example, users with vestibular (inner ear) disorders might experience nausea, dizziness, or headaches if there is excessive movement on screen. Having the ability to turn off these animations would improve the user’s experience.

Animations included in this success criterion include parallax effects when scrolling, where the page foreground and background move at different speeds or in different directions, and animations triggered by user clicks.

There are exceptions to this rule: animations that are essential to the functionality or information being conveyed. For example, basic page scrolling is considered an essential function and is excluded from this requirement. 

Another example is web pages where animations are a part of the purpose of the page. For instance, online platforms for creating slide decks with transitions between slides, or where users create the animation themselves.

You can provide the ability to turn off non-essential animations in multiple ways:

- Place a button/toggle on the web page that gives users the option to disable the animations.
- Use the "prefers-reduced-motion" CSS media query (this option has limited-but-growing support). Users can set a preference for reduced motion in their operating system (not their web browser), which web browsers can then indicate to web pages. As of April 2019, the "prefers-reduced-motion" media query is supported in Safari on desktop and mobile, in Firefox on desktop, and is included in the beta for Chrome 74.
However animation is reduced or removed, ensure that it does not prevent users from accessing content on the page.

Note that this success criterion specifically pertains to animations that are "triggered by interaction," meaning as a result of user actions. SC 2.2.2 Pause, Stop, Hide (level A) governs page information that scrolls, blinks, or moves automatically without user interaction, as well as auto-updating content.