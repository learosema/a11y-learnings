# Keyboard instructions

## Overview

What if your JavaScript widgets are 100% keyboard-accessible, but people don't know how to use them?

You could say, "well, that's the user's fault," and maybe it is, but maybe it's just because there are so many possible ways of creating the same type of widget that the user simply doesn't know what design pattern you're using. This can be true especially with ARIA widgets that follow the ARIA authoring practice recommendations.

## Users may not expect or be aware of ARIA keyboard patterns

ARIA widgets are supposed to follow native desktop design patterns. That's one of the selling points of ARIA. The idea is to make the web act more like "real" applications, to give us more consistency across our experiences in native applications and web applications.

ARIA design patterns also save us keystrokes, because the pattern is to tab into the widget, and then use the arrow keys (not the tab key) to navigate around within the widget, allowing us to use the tab key to move past the widget with a single keystroke.

Tab once to get into the object, and tab again to get out of it.
Navigating around within the object is optional, and is done with the arrow keys, but only if we want to.

This "new" pattern (at least it's sort of new to the web) is a good idea, but not all users expect it, mostly because most web sites don't use this pattern yet.

As more web sites begin to use this pattern, users will get used to it, and they'll adapt, but right now we're in a transition period where only a few web sites use this pattern, and most do not. Users still expect to use the tab key to navigate everywhere in a web site.

## Should You use ARIA keyboard patterns?

The mismatch between the user's expectations (to use the tab key) and the web designer's good intentions (to use ARIA best practices which recommend using the arrow keys) can cause some confusion, and it can make some users mistakenly believe that the widgets are not keyboard-accessible, even when they are.

Some people use this as an argument against using ARIA keyboard patterns. The problem with this logic is that if everyone delays until most web sites use ARIA keyboard patterns, no one will ever implement ARIA keyboard patterns.

Let's flip it around: The sooner websites adopt ARIA keyboard patterns, the sooner users will expect them when they come to your website. It turns out that keyboard users are already used to using these conventions in the operating system, so it isn't as much of a stretch as you might think for them to learn to use those keyboard patterns on websites.

Even so, giving users a little extra information, in the form of some brief instructions, may be a good idea.

## Consider providing brief instructions for keyboard users

When you do start using ARIA keyboard design patterns, you may want to consider giving keyboard users some prompts to let them know how to interact with your JavaScript widgets. Keep in mind that there are two main audiences with keyboard accessibility:

- Sighted keyboard users
- Blind screen reader users

There is a tendency for developers to forget sighted keyboard users, so make sure you don't do that. The message can be short. It could say things like:

- "Use your arrow keys to navigate the tree menu."
- "Use your down arrow key, followed by the enter key to select from the drop-down list."
... and so on. Keep the instructions brief.

Here are some possible ways to provide keyboard instructions:

- Write the instructions above the widget for everyone to see.
- Make the instructions appear as a pop-up tooltip when the widget receives focus. Use aria-live to announce the text in the tooltip.
- Make the instructions appear as normal text when the widget receives the focus. Consider adding an outline or background color to draw attention to the text for sighted users. Use aria-live to announce the text.

You may be able to come up with other ways to instruct the user of the keyboard pattern. Just be sure that you're actually using a standard pattern to begin with, and be sure your methods work for both sighted keyboard users and blind screen reader users.