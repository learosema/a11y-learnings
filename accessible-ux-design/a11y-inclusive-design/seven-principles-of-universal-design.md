# 7 Principles of universal design

## Overview

There is a set of principles and guidelines for universal design, written in 1997 that is worth knowing about.

A group of architects led by Ronald Mace at North Carolina State University called into question approaches to designing buildings, products, and environments.

Realizing that spaces and products should be designed for universal use, the group of architects developed seven principles to guide those working in the field in universal design. Tthese principles have been a point of reference to applying universal design to other areas such as education and web design.

See also: [The Principles of Universal Design](https://www.ncsu.edu/ncsu/design/cud/pubs_p/docs/poster.pdf)

Note: guidelines are quite subjective, it's difficult to write algorithms for that.

## Principle One: Equitable use

The design is useful and marketable to people with diverse abilities.

### Guidelines:

- 1a. Provide the same means of use for all users: identical whenever possible; equivalent when not.
- 1b. Avoid segregating or stigmatizing any users.
- 1c. Make provisions for privacy, security, and safety equally available to all users.
- 1d. Make the design appealing to all users.

### Good example on the web

- A web site uses semantic markup in all the appropriate places (headings, landmarks, table structure, form labels, etc.) and creates a single design that works well for users who are sighted as well as for users who are blind.

## Principle Two: Flexibility in use

The design accommodates a wide range of individual preferences and abilities.

### Guidelines

- 2a. Provide choice in methods of use.
- 2b. Accommodate right- or left-handed access and use.
- 2c. Facilitate the user's accuracy and precision.
- 2d. Provide adaptability to the user's pace.

### Good examples on the web

- a drag-drop widget that is designed to work with any of: mouse, keyboard, touchscreen
- websites warning the user 2 minutes before the session is about to expire and give the user the option to extend the session. The warning is fully accessible to screenreader users

## Principle Three: Simple and Intuitive Use

Use of the design is easy to understand, regardless of the user's experience, knowledge, language skills, or current concentration level.

### Guidelines

- 3a. Eliminate unnecessary complexity.
- 3b. Be consistent with user expectations and intuition.
- 3c. Accommodate a wide range of literacy and language skills.
- 3d. Arrange information consistent with its importance.
- 3e. Provide effective prompting and feedback during and after task completion.

### Good examples on the web

- news site includes a simplified summary
- form validation that provides clear success confirmation messages and clear error messages. Ensure screenreader users get full benefit of the messages
- structured content with headings that clearly mark the important sections of the content
- Ads are clearly marked as such and are placed out of the main flow.


## Principle Four: Perceptible Information

The design communicates necessary information effectively to the user, regardless of ambient conditions or the user's sensory abilities.

### Guidelines

- 4a. Use different modes (pictorial, verbal, tactile) for redundant presentation of essential information.
- 4b. Maximize "legibility" of essential information.
- 4c. Differentiate elements in ways that can be described (i.e. make it easy to give instructions or directions).
- 4d. Provide compatibility with a variety of techniques or devices used by people with sensory limitations.

### Good examples on the web

- A tutorial on how to tie your shoes is presented in text, illustrations, and video with narrated instructions.
- ARIA live announcements are used to announce to screen reader users the number of available options in a custom ARIA/JavaScript autocomplete drop-down list (e.g. "There are three cities that start with 'SAN.' Use the down arrow key to navigate the options").

## Principle Five: Tolerance for Error

The design minimizes hazards and the adverse consequences of accidental or unintended actions.

### Guidelines

- 5a. Arrange elements to minimize hazards and errors: most used elements, most accessible; hazardous elements eliminated, isolated, or shielded.
- 5b. Provide warnings of hazards and errors.
- 5c. Provide fail safe features.
- 5d. Discourage unconscious action in tasks that require vigilance.

### Good examples for the web

- Financials web site confirms "are you sure you want to transfer funds?" before funds are transferred, in case users pressed the button by accident
- A CMS places "deleted" items in a recycle bin and allows users to recover them later if they change their mind.
- A search feature performs a spell check on submissions and suggests corrections.

## Principle Six: Low Physical Effort

The design can be used efficiently and comfortably and with a minimum of fatigue.

### Guidelines

- 6a. Allow user to maintain a neutral body position.
- 6b. Use reasonable operating forces.
- 6c. Minimize repetitive actions.
- 6d. Minimize sustained physical effort.

### Good examples for the web

- A web site has a "skip to main content" link at the top, allowing keyboard users to avoid tabbing through all of the links in the header and navigation.
- A web site has good heading and landmark structure (importantly, the content starts with an <h1> heading, inside a <main> landmark, among others), allowing screen reader users to navigate by headings and landmarks to the part of the page they're interested in.

## Principle Seven: Size and Space for Approach and Use

Appropriate size and space is provided for approach, reach, manipulation, and use, regardless of user's body size, posture, or mobility.

### Guidelines

- 7a. Provide a clear line of sight to important elements for any seated or standing user.
- 7b. Make reach to all components comfortable for any seated or standing user.
- 7c. Accommodate variations in hand and grip size.
- 7d. Provide adequate space for the use of assistive devices or personal assistance.
