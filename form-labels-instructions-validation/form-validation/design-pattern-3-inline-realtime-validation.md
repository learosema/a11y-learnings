# Design Pattern 3: Inline real-time validation

## Overview

Inline (real-time) validation can be used to communicate to users if they are filling in a form field correctly or not.

## Implementation Details

### Aria-live Announcements

When using `aria-live` for real-time announcements, it is important that users aren't subjected to constant aria-live announcements, especially after every keystroke.

This can get in the way of a screen reader's audio output to users. The model in the example on this page sets a timer that waits until the user isn't typing for 2 seconds, then makes the announcement.

Also, trying to use aria-live on blur (upon leaving a field when there is an error) is almost always as bad because the screen reader will start reading the next item that is in focus at the same time — meaning there are two competing events.

The aria-live announcement will probably lose that contest, so users won't hear the announcement.

### Screen Reader Users

For users who are blind and other screen reader users, it is acceptable to wait until the user submits the form to find out that there are errors.

It is true that sighted users will see the errors sooner, but the usability problems with real-time validation are too great for screen reader users in most instances to try to achieve that for them.

Many screen reader users will explore a form first before filling it out. When they explore a form, they may put the keyboard focus in a form field, then leave the form, which can trigger a blur event. If the form has a lot of validation triggers tied to blur events, a screen reader user may trigger them all.

As a result, the form is full of validation errors before the user has filled out the form. When they go back through the form, they may encounter all of those errors. In most cases, it will just be annoying. However, if the form causes a context change or has other dynamic responses to blur events, the act of exploring the form can cause more significant problems for the users.