# Defining a11y as the minimum goal

## Overview

Making a web site accessible, or available, to people should be the minimum goal. Yes, you want people to have access, but you also want them to have a good experience. You want them to find the experience usable, intuitive, compelling, and enjoyable.

## Strengths and limitations of guidelines

Guidelines as WCAG 2.1 play a great role in creating accessible content. They are the core foundation.

But: you can fully comply with the a11y guidelines and your design is not fully accessible (though the risk of having a terrible inaccessible site when following the guidelines is low).

The guidelines don't cover every last aspect of a11y. They are created with objective testability in mind.

The category of disability most neglected in current guidelines is cognitive disabilities, because many of the measurements of cognitive disability access include some degree of subjective judgment.

## Objective a11y guidelines

Many asoects of a11y are objectively testable, eg.

- images must have an `alt` attribute
- all form inputs must have a label
- header cells of a table must be marked as header cells using `<th>`
- the page must have a `title`
- Color cannot be used as the only visual means of conveying information

These are easily verifiable, the web page either passes or fails on these points and some of these points are even automatically testable

## Subjective a11y guidelines

- Use visual cues to focus the user's attention on the main purpose of the web page. (This is an important principle of message design and of interaction design, especially for users with cognitive disabilities, but how do you measure the degree to which the user's attention is focused?)
- Ensure the font is easily readable. (How do you define "easily?" At what point do you draw the line to designate one font as easily readable and another as not easily readable, and what criteria would you use in making that judgment?)
- Minimize the cognitive skills required to use the web page. (How do you measure the degree of cognitive skill required to complete a task? At what point would you draw the line and say a certain task requires too much cognitive skill?)

Many of the subjective criteria spill over into areas that many would consider the realm of usability, rather than pure accessibility, but the truth is there is a lot of overlap between accessibility and usability. What if a website is technically "accessible" (according to the guidelines) but is highly unusable? Could you really say that such a web site is accessible? It might meet a limited definition of accessibility, but it would fail to meet the implied intent of web accessibility, which is that people with disabilities can use the web site.

## Ideas that should have been in the guidelines

WCAG 2.0 became an official recommendation in 2008. They've had a lot of time to practice and discover weaknesses.
What we've learned is that there are three main categories in which WCAG 2.0 can be improved. In fact, the W3C created task forces to review each of the following areas:

- Cognitive Disabilities
- Low vision
- Mobile and touch devices

WCAG 2.1 (released 2018) addressedmany of these a11y gaps in WCAG 2.0 with 17 new success crieteria.

## Reaching beyond the guidelines

- create the best experiences possible for people with disabilities
- compliance is important. Keep in mind it's the bare minimum
- create experiences that people with disabilities actually enjoy, not just experiences they merely tolerate
