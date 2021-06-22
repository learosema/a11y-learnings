# Timers with fixed deadlines

## Timers with fixed deadlines SHOULD provide users with a dynamic countdown feature, especially if the deadline is soon.

A dynamic countdown feature counts down to the deadline in real time. This allows users to get a sense of the urgency of the deadline, and to act accordingly.

<b>Important</b>: Screen readers will read the text of the timer as static text and will not provide live updates unless ARIA live regions are also used. The user can navigate away from the timer then back to it to hear the most current time remaining, but live updates are not automatic.

## Countdown features SHOULD post ARIA live announcements at strategic intervals.

Screen reader users can benefit from live announcements of the time remaining, especially as the deadline gets closer. If a user is taking an hour-long test, for example, the timer could notify the user at 15-minute intervals, at 2 minutes remaining, and at 1 minute remaining. That would be reasonable.

### Example

In this example, the deadline is very soon: 40 seconds from the time the page loads. There are ARIA live announcements every 10 seconds, and also at 5 seconds remaining.

The frequency of announcements in this particular example is exaggerated a bit for instructional purposes (so you can experience the ARIA live announcements). In most cases, you would provide fewer announcements, with more time in between them.

- [Example with aria alerts and page title updates](https://dequeuniversity.com/assets/html/module-dynamic/deadline/good/index.html)

- Note 1: Also note that the page title is updated dynamically with the time remaining.
- Note 2: When the timer expires or when the user activates the "Purchase" button, the focus moves to the message so that screen reader users will hear it. This is especially important in this case because the "Purchase" button disappears. If the keyboard focus is on the button when it disappears, the focus will most likely be lost, returning to the top of the page. Moving the focus to the message ensures the focus will not be lost.


## Countdown features MUST NOT post ARIA live so frequently that they become overwhelming to screen reader users.

There is no exact rule on how frequently to post ARIA updates, but you should think through the user experience and take into account how critical it is to know the exact time remaining. Every context is a little bit different.

What you don't want to do is post announcements so frequently that screen reader users have a hard time listening to the rest of the page. You don't want to cross into annoyance territory.

## If the timing is critical, a dynamic countdown MAY be included in the page `<title>`.

The page `<title>` is the first thing screen reader users hear. If the deadline is soon, it can be helpful to hear the time remaining immediately when the page loads. If the deadline is not so soon, it is less critical to add a dynamic timer to the page `<title>`.

## If the timing is critical, the dynamic countdown timers and alerts SHOULD be included across all relevant pages on the site.

Think holistically about the web site overall. If the web site is an auction site or a ticket sales site, or any kind of site where deadlines are critical, consider including a dynamic countdown timer on all relevant pages, including ARIA live updates and page title updates where appropriate.