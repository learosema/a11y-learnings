# Defining affordances

## James J. Gibson's original concept of affordances

Psychologist James J. Gibson coined the term "affordances" in 1977 to refer to the range of possible actions that someone can perform with a particular object. Here are some examples:

### Example: The affordances of doors

A door affords the possibility of being opened, of allowing passage from one side of a wall to another. Depending on the door's design and placement, a door could offer the affordance of being pushed, pulled, or sliding to the side.

### Example: The affordances of coffee mugs

A coffee mug affords the possibility of holding things, especially, but not limited to, liquids. If it has a handle, it affords the possibility of being gripped in a place that isn't hot (if the cup holds a hot liquid) and affords the possibility of being hung on a peg by the handle.

## Affordances for whom?

A key concept in Gibson's idea of affordances is that an object's affordances depend on a person's action capabilities, which can vary one person to the next. What are the affordances of an object? There is not one universal answer. You have to ask: affordances for whom?

This is where the concept of affordances begins to enter in the realm of accessibility.

### Example: The unequal affordances of stairs

The affordances of stairs depend on a person's mobility.

A fully mobile person: Stairs afford the possibility of moving from one level to another, either up or down.
A wheelchair user: Stairs do not afford wheelchair use, so they do not afford the possibility of moving from one level to another. 

Stairs may afford less obvious things to a wheelchair user, such as alerting them to the fact that there are multiple levels, or possibly letting them look up or down at part of the next level. But stairs do not afford wheelchair users the main purpose of their design. Stairs simply aren't designed for wheelchair users.


### Example: The unequal affordances of computer screens

The affordances of a computer screen depend on a person's vision.

- A sighted person: A computer screen affords the possibility of perceiving visual interfaces and interacting with them using visual input methods, such as mouse or touch.
- A person who is blind: Computer screens don't really afford anything useful to a person who is blind. They cannot perceive the visual output nor use visual methods of interacting with the visual interface.
Affordances are binary (according to Gibson)

Once you take into account both the object and the person's action capabilities, the affordances of an object are a binary property of the object: they either exist or they do not. Even if a person does not know all of the affordances of an object, the object still has all of those affordances. An object's affordances do not depend on the person's ability to recognize them.

### Example: The secondary (unintended) affordances of a volleyball

Volleyballs are designed to be hit with the hands during a volleyball game. That is the most obvious affordance of a volleyball, but for most people, volleyballs afford other possibilities too:

- A volleyball can be kicked.
- A person can sit on a volleyball.
- A volleyball can be used as a flotation device in an emergency (though this is not recommended as its primary purpose!)
- A volleyball can be used to break a window (this use is also not recommended under most circumstances!).
A person can draw a face on a volleyball and use it as the head of a scarecrow (not a common use, but somebody might do it!).

You get the idea. A volleyball affords lots of possibilities beyond its primary purpose. Gibson's concept of affordances takes all of these possibilities into account.

## Donald Norman's Human-Computer Interaction (HCI) concept of affordances

Starting in 1988, Donald Norman began to use the term "affordance" in a design context within human-computer interaction (HCI). His use of the term was similar to Gibson's use, with a few important nuanced differences. According to Norman, the following are true:

An object's affordances are dependent on the perceivability of the affordances. If a person cannot perceive an affordance, the affordance does not exist for that person. (By way of contrast, Gibson would say that the affordance exists whether a person can perceive it or not.)

A person's perception of affordances is influenced by the person's culture, background, education, and other relevant experiences and characteristics.

The affordances of an object can be designed to be obvious — and therefore usable and useful — or the design can obscure or inhibit affordances. For Norman, design quality is key to giving an object the intended affordances.
Donald Norman took the original idea of affordances and turned it into a design goal: Objects should be designed to offer the right kind of affordances.

### Good example: A door handle with obvious "push" and "pull" affordances

One of the classic examples of design affordance is doors.

If a door is designed to swing open in only one direction, then one side must be pushed and the other side must be pulled. The visual appearance of the door should make it obvious which action should be performed on which side. By putting a "pushable" metal plate on one side and a "pullable" handle on the other, people won't have to think about which action to perform. They will perform the action that the side of the door affords them.

A door with a push plate on one side and a pull handle on the other

### Bad example: A door handle with ambiguous or misleading affordances

If you design a door with "pullable" handles on both sides, people will probably assume that they need to pull the handle to open the door, even when they're on the side that they need to push. Norman would say that the door's design lead people to believe that the door affords "pullability" on both sides, even though the reality is that only one side is pullable.

A door with pull handles on both sides; one side says push and the other side says pull

## Web design affordances

Web designs can also be analyzed in terms of the affordances they offer (or fail to offer).

### Bad example: Editable text inputs that do not look editable

In the example below, there are three text fields, one for entering your name, one for entering your email, and one for entering your phone number. The fields have been visually styled with no borders or visual differentiation at all, so it is not obvious where a person should click the mouse to start typing.

- Name:
- Email:
- Phone:

It turns out that the text inputs in the above form are below the labels, which may be unexpected for some visual users who may expect the text inputs to be immediately to the right of the labels. Even if the user guesses correctly, why make the user guess at all? The text inputs should be designed in a way that makes their affordances obvious.

Poor design decisions can restrict affordances to only users who have no disabilities. This is especially true when dealing with custom JavaScript controls.

### Bad example: A custom link without link affordances for some users

In the example below, there is a link which has the appearance and behavior of a link for sighted mouse users, which means that it affords sighted users "clickability" and the expectation is that the link will take them to the destination named in the link. All of those expectations turn out to be true for sighted mouse users.

Here is a link to <span style="color: blue;">Wikipedia</span>.

But this link was created using CSS and JavaScript, not using a standard anchor element (<a>), and no additional accessibility attributes (i.e. role="link" and tabindex="0") have been applied to it, so keyboard users will not be able to tab to the link to activate it, and screen reader users will not be able to identify the text as a link at all.

This contrived link does not offer the affordances of a link to keyboard users or screen reader users.

## Designing with affordances in mind

For our purposes in this module, Donald Norman's design-oriented interpretation of the concept of affordances gives us a little more to work with as we consider user needs in our web designs. We want to make the purpose and functions of our designs (the affordances) obvious to all of our users, not just to fully-able-bodied people.

<b>Perceivable affordances</b>: Users have to perceive the affordances of an element to be able to use it. Perception capabilities vary from one person to the next:

- A person who is sighted will perceive affordances mainly through visual recognition.
- A person who is blind will perceive affordances mainly through sound (via a screen reader) and will discover the affordances via the semantic structure (names, roles values) of the elements in the web design.
- A person who is deafblind will perceive affordances mainly through touch (via a refreshable braille device), and, like people who are blind, will discover the affordances through the semantic structure of the web design.
- A person who is deaf will perceive affordances mainly through visual recognition, and, for the most part, will not experience disability-specific problems perceiving affordances in the interface, but will definitely experience accessibility issues with video and audio content, if there are no captions or transcripts.
