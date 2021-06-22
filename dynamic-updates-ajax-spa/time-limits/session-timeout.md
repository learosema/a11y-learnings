# Session Timeout

## If there is a session time limit, users MUST be warned before the session ends and MUST be given time to save their data and/or extend the session.

A session must never end without a warning. One of the most effective ways to warn users is with a dialog, giving the user the choice to extend the session or to allow it to expire. The warning should appear with plenty of time left for the user to respond. A two-minute warning is generally considered sufficient under most circumstances.

- [Good example with warning and option to extend session](https://dequeuniversity.com/assets/html/module-dynamic/timeout/good/index.html)
- [Bad example, expiring session without warning](https://dequeuniversity.com/assets/html/module-dynamic/timeout/bad/index.html)

## Incomplete data SHOULD be saved after a session timeout.

When a session ends prematurely for a user, there is a risk of data loss. Even if the website warns the user about the timeout, other events may intervene to cause the user to not be able to extend the session.

The user may need to step away from the computer to attend to other business, for example, or may be distracted by other things happening in the room. Just because the user doesn't extend the session, you shouldn't assume that the user has chosen to abandon and permanently lose her data.

Even if the user is warned ahead of time about the session timeout, the user may not realize that data might be lost when the session ends.

If a user has started to enter data in a form, whenever possible, the website should be scripted to save the data when the session ends, so that the user can retrieve the data after starting a new session and have the option of picking up where she left off. 

This is especially true when the user is in the middle of a lengthy process, such as filling out a tax return, or a mortgage application, or writing a long message.

Sometimes saving the data is not possible, not practical, or not advisable, but those circumstances should be considered exceptions, rather than the rule.

## Users SHOULD be warned of the duration of any user inactivity that could cause data loss, unless the data is preserved for more than 20 hours when the user does not take any actions.

If a user unintentionally takes too long to a complete a task or leaves the page inactive for a period of time, it is frustrating to have to start a task all over again. To avoid this, you can:

- Give the user at least 20 hours, regardless of inactivity, to complete the task or form.
- Inform the user of the inactivity time constraint at the beginning of the task so that they can choose to prepare their information ahead of time (so they don’t need to run and find more documents to complete their taxes, for example, risking an inactivity timeout), and make sure any breaks they take or pauses they use to check their work are not too long.
- Save user information. However, various privacy policies and laws affect this solution (such as obtaining explicit user consent), so the W3C recommends consulting experts on privacy and legal counsel before using that solution.

Note that this success criterion does not apply to content that is timed regardless of inactivity. Timed content is covered by SC 2.2.1 "Timing Adjustable."