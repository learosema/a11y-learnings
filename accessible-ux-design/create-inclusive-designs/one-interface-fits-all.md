# One interface fits all?

## Overview

Is it possible to design a single interface to satisfy all of the needs of all of the different types of disabilities?

The honest answer is that no, especially when you take into account the full range of cognitive disabilities — but you may be surprised at how much one design can accomplish.

In fact, the best approach for almost every circumstance is to create a single, inclusive design, rather than try to create multiple designs for different types of disabilities.

## One web design is almost always enough

There are strong arguments for not creating separate designs just for the sake of accessibility:

- Separate designs are rarely necessary: You can build in all of the a11y in a single design for almost all kinds of disabilities (severe cognitive disabilities are the main exception).
- Users may not activate the accessible version: Even if you create "perfect" accessible versions for every possible type of disability, how will users know that those versions exist? It is much easier for a person to simply use the web site than to try to figure out custom accessibility options or how to activate them
- Stigma: Not being able to use the main site and having to use an accessible version of the site is inconvenient and stigmatizing. 
- Maintenance nightmare: Maintaining one version of a web design is hard enough.
- You can't tell who has a disability: There is no way to automatically detect which users have disabilities and which don't.

## Room to innovate: Is it ever a good idea to create separate designs for accessibility purposes?

The answer is almost always NO: don't create separate designs.

Despite all of the strong arguments against creating separate designs, there are some legitimate circumstances in which having separate designs could be beneficial. The most obvious is the use case of people with cognitive disabilities. They can benefit from a separate design that simplifies things, focuses their attention better, and provides extra help when needed.

Sometimes it would also be helpful to know when a person is using a screen reader, so that certain features could be turned on or off based on the need to make them available to screen readers. Usually that's not necessary, because most screen reader accessibility features are "under the hood" in the markup, so they don't affect other users. But every once in a while, a screen reader accessibility feature will encroach a little bit on the visual design.

### Important warning

This whole discussion of how to achieve separate high quality optimized designs for different types of disabilities is NOT practical or advisable under most circumstances. We're discussing it here in terms of theoretical possibilities, to stimulate thought for possible future innovations.

Proceed cautiously with any of these lines of thought. They have the potential to do more harm than good when applied inappropriately, incompletely, or incompetently. The safer choice, by far, is to create a single accessible design.


### Detecting screen readers

- not possible, and there are good reasons for that
- in theory, screen reader detection could be done well and to good effect, allowing developers to create optimized content benefitting screen reader users.
- It may never happen, and in fact many screen reader users hope that it never happens, because of the fear that the feature will be abused, or that developers will look at the web server logs and conclude that too few screen reader users actually use their site for them to care about accessibility. Screen reader users don't want the information used against them.

Contra: 

- maintream browsers and screen readers would need to support screen reader detection
- it would take time to become widely available
- you should almost never use this feature. It should be reserved for special cases when it is difficult to achieve screen reader accessibility in a mainstream design. Special cases are:
  - responsive tables or grid systems, both of which can be problematic for screen reader implementations
  - unusual custom widgets
  - when trying to work around known screen reader deficiencies
- you would almost never want to create a different page for screen reader users

### Making it easy to use

By far the biggest challenge with the idea of creating separate versions optimized for people with disabilities is figuring out how to provide the separate versions in a way that is easy to find, easy to activate, and easy to use.

People with cognitive disabilities are the ones that could benefit most from a separate version, yet they are the ones that are least likely to be able to find and activate accessibility features on their own.

It's worth mentioning that some people with cognitive disabilities require the assistance of another person while doing things like using the web, so in those cases it would probably be the assistant who activates the accessibility features, but you can't count on that.

#### Possibility 1: Add accessibility customization to the website itself.

You can add things to the website's interface like:

- A button to enlarge the font size (for people with low vision)
- A button to increase the contrast (for people with low vision)
- A button to switch between the mobile and desktop view (for people with low vision or with cognitive disabilities)
- A button to switch between a simplified version of the content (e.g. less text and/or simplified wording) and the full version (for people with cognitive disabilities)
- A button to read the text out loud — basically an on-demand screen reader — using products like BrowseAloud (for people with low vision or cognitive disabilities or reading disabilities)
... and other possible on-the-spot enhancements

All of these are fine ideas, and if you want to implement them, you should. Be sure to save the user's preferences somehow, either in a session cookie or in the user's profile in a database, if the site stores user information on the server. There are limitations to this approach though:

- The settings impact only the current web site. They are not transferable to other web sites.
- The settings are not transferable across browsers, unless the information is stored on the server and the user is required to log in.
- Users don't expect to find accessibility controls on web sites themselves, so they may not realize what they are at first, and may not use them.
- Most of the time, users who truly need those kinds of features will implement them some other way, using settings in the operating system or using third-party software. In a sense, adding accessibility options like that to a web site are redundant, because there are other ways of doing the same thing across all web sites.
- If people are already using other methods, like a screen magnifier with high contrast settings turned on, the custom user settings on the web site will probably be overridden or altered by the user's other methods, so users won't experience the intended effect (unless they turn off their other settings).

There are also some positive sides to this approach:

- Putting accessibility controls on the web site highlights accessibility and shows that the web site owners are at least aware of accessibility.
- The web site designers can create settings that are relevant to their specific design. In theory, when done well, the designers should be able to create a better experience than generic settings in the user's preferences in the operating system or assistive technology.
- People with minor disabilities who don't need the full set of options in the operating system or assistive technologies can turn on the accessibility features if they want, without having to invest the time or money in installing, learning, and using assistive technologies.
- Taking into account the limitations and positive sides, you can certainly choose to do things this way as long as the default version of the web site is still as accessible as possible. Don't create an accessible version and an inaccessible version. That would fly in the face of the whole idea of inclusive design. Instead, use these ideas as optional enhancements, not as your main accessibility strategy.

#### Possibility 2: Add accessibility preferences to user profiles in the browser.

Browsers could store user preferences in the settings and pass on this information to the web server via a user agent string or through some other similar mechanism. 

Many browsers these days allow users to sign in to a central server and use the same preferences across devices, which could be a convenient way to avoid having to alter the settings every time the person uses a new device.

#### Possibility 3: Add accessibility preferences to user profiles in the cloud.

A third option would be to store the user's preferences in the cloud through some sort of third-party web site and convey those settings to the web server via an add-on feature in the browser, appending information to the browser's user agent string or through some other mechanism. This solution has the benefit of working across more than one brand of browser.

#### Privacy concerns

With all of these possible approaches, there are privacy concerns. What if the person does not want to disclose their disability? Could the information be used against them? Is it anybody else's business to know if the person has a disability? You should take these privacy concerns seriously. Ideally, information about the user's disability-related preferences would be stored anonymously and separately from other user data.
