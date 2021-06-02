# User Research with people with disabilities

## Overview

Learning directly from users with disabilities can be one of the most valuable things you can do as a part of the design process. It's one thing to read through a checklist of items and implement them. 

It's quite another thing to actually experience the design as a person with a real disability. If you don't have a disability yourself, you don't know what it's like. You can only guess. 

You'll get more accurate in your guesses as you gain experience, but seeking feedback from users with disabilities will always be valuable.

## Fix what you know how to fix first

Before seeking feedback from people with disabilities, make sure your site is compliant. You don’t want to waste the person's time identifying obvious accessibility issues. Pay close attention to:

- Automated test: use automated tooles like axe
- Keyboard accessibility: tab through the page and activate features. Find out if the page is functional without using a mouse
- Test the site with a screen reader (eg. VoiceOver)

There's a lot more you can do beyond these two things, but you don't need a person with a disability to tell you you're missing alt text on an image or a <label> for a form element, for example. Automated tools can already do that. Take advantage of the person's time to gain more meaningful feedback.

## Pay attention to usability feedback

Users with disabilities are likely to identify a combination of accessibility problems and usability problems. Some of the first things you will probably hear are "this is confusing," or "I'm not sure how to do this." 

You may observe a person using a screen reader and realize that they are navigating all around where you want them to go, but they're unsure of what they're supposed to do, or unsure of how to find what they need to find. 

It may be right in front of them, and it may even be technically accessible, but it's not organized in a way that they expect or understand.

In fact, let's take it to the extreme: let's say that ALL of the feedback is related to usability concerns, and that there are no accessibility guideline failures, as verified by an experienced accessibility expert. Do you have to fix the usability concerns to be able to say your site is accessible?

First of all, celebrate the fact that you met all the accessibility guidelines! That's a noteworthy accomplishment.

Second, dig deeper. Is this the best your site could be? Put yourself in the position of the person with the disability. How hard was it for that person? If you had the same disability, would you consider your design to be a good design for yourself? Would you be satisfied?

### Usability affects a site's perceived accessibility

If a web site is difficult to use, it's not always obvious to people with disabilities whether the problems are due to accessibility compliance errors or broader usability problems. If they can't figure out how to use your web site, they may assume your site is inaccessible, even if it is technically compliant but just hard to use with a disability. Design a good, usable experience so that people don't have a reason to question the site's accessibility.

## Record screen videos of people with disabilities using the site

You can learn a lot about the usability of your site by recording a person with a disability using it.

1. Choose a pathway through your site that you want to evaluate, such as:
  - Searching through products, choosing one, and adding it to the shopping cart
  - Purchasing items in the shopping cart
  - Creating a user profile
  - Choosing a seat on an airplane
  - Choosing the hardware configuration for a new computer purchase
  - Using an educational simulation in an online course
  - Transferring funds from one account to another
2. Set up screen recording software on the person's computer.
3. Set up a separate video camera to record the person's actions and facial expressions, to capture data that might not be evident in a screen video.
4. Record the person narrating his/her thought process and reactions while navigating. Encourage the person to talk through things in as much detail as possible, mentioning keystrokes they're using, what they expect to happen, noting anything that is unexpected, and explaining whether they use this same pattern frequently, or if they're being more exploratory or experimental than usual. It's usually best to not be in the room while the person is recording the video, so that you aren't tempted to give them any hints as to how to complete a task if they get stuck.
5. Watch the videos on your own and note the parts that were difficult and why they were difficult.
6. Discuss the experience with the user to gain additional insight.

## Which typeof disabilities should you include?

- in an ideal world, all, but that's not practical in the real world
- try to get feedpack from people with as many different types of disabilities as possible

### Learn from people with different types of disabilities

- Screenreader users help you understand whether or not your semantic structure is adequate, whether your videos are understandable when you can only listen to them, and how keyboard-accessible the site is.
- Screen magnifier users can help you understand the low vision experience, including things like the quality of your responsive design, the importance of large click target size, the importance of good contrast, and whether or not the site is usable in high contrast mode.

## Every person with a disability is unique 

- Don't overgeneralize
- Take the person's feedback seriously, but don't take it as single source of truth
- it OK to get a second opinion
- there are many variables regarding your tester
  - tech experience
  - prior experience with your web site
  - level of experience using assistive tech
  - amount of time the person has had the disability
  - comfort level and past experience providing user feedback
  - ability to explain themselves well
  - creativity when confronted with an a11y barrier
  - relationship with you
- all factors can influence the quality/type of feedback you get
- sometimes one user feedback session is enough, sometimes you need four or five sessions