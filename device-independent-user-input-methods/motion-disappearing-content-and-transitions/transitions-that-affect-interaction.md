# Transitions that affect interaction

## Transitions MUST NOT interfere with reading or interaction, unless the interference is brief.

Animated transitions that occur on a web page must not interfere with a user reading a web page or interacting with a web page. Slow transitions (transitions that last longer than 5 seconds) on a web page can be distracting for users with cognitive disabilities and may cause dizziness in users who are sensitive to motion.

Additionally, assistive technologies like screen readers may begin rendering the web page content before a slower transition is complete, thus causing screen reader users to miss content that is contained in the transition.

Fast transitions (transitions 5 seconds or shorter) may be used as long as they do not interfere with web page reading and interaction.

### Good example

In this example, there is a notification that slides down from the top of the screen in half a second, while pushing the rest of the page downward.

The speed of the transition minimizes any difficulty in reading or interacting with the web page. The fact that the notification is relatively small also minimizes the impact on reading and interaction.

- [Open the good transition example](https://dequeuniversity.com/assets/html/module-input-methods/transitions/goodtransitionexample.html)

## Transition effects SHOULD be kept to a minimum (to avoid nausea, dizziness, annoyance, etc.).

Though quick transitions can be used on a web page, it is important to remember that transitions need to be used at a minimum to prevent too many distractions on a web page. Plus, frequent use of transitions may cause motion sickness or dizziness in users who are sensitive to movement.

## Parallax effects SHOULD be kept to a minimum, in terms of the total number of parallax effects, the amount of parallax within each individual effect, and the size of the area affected.

The more parallax effects you include, and the more extreme they are, the greater the risk that you'll cause problems for people with vestibular disorders.