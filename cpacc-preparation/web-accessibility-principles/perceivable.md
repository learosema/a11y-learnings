# Perceivable

## Defining Perceivability

Perceivability is about making the output of web content available through multiple sensory modalities.

## Biological Pathways to Perception

You have to be able to perceive web content through at least one of your biological senses for it to be accessible at all. As a quick reminder, these are your five senses:

1. Sight
2. Sound
3. Touch
4. Taste
5. Smell

Of these, we're really only concerned about the first three: sight, sound, and touch. Someday someone may invent a way to taste or smell the web, but until then, we can safely assume that we don't need to worry about the flavor or scent of our web pages.

## Seeing Web Content

Most people perceive web pages by looking at them. Your eyes focus the information onto photo-receptors in your retina, and your brain translates that raw visual stimulus into meaningful information. This works well for everyone who has good vision, but not so well for those who do not.

The majority of web developers and web designers are relatively young and able-bodied, so they design web content that works for people just like themselves. Often developers and designers don't even realize that some people can't see the content at all, so they don't build in other ways to perceive the content into the designs.

## Hearing Web Content

People who cannot effectively perceive visual information—because they are partially or completely blind—need to perceive web sites some other way. Most blind people can hear, so sound is the most effective alternative method of perceiving web content for the majority of people who are blind.

Screen reader software converts the digital text into synthesized speech, allowing blind people to listen to web content. Listening to web content is a fundamentally different experience from looking at web content, just as hearing someone describe an event is fundamentally different from watching it, but different does not necessarily mean bad, unless the experience is not parallel, or functionally equivalent.

People who are blind are used to listening rather than seeing, so listening to web content is a logical and natural approach for them.

## Feeling Web Content

For those who cannot see or hear adequately to view or listen to web pages, there is one more sensory modality available: touch. Digital text can be converted to three-dimensional braille characters that a person can feel with the hands. Traditional braille is printed on sturdy paper, with raised dots configured in an alphabet of characters and symbols. 

Modern refreshable braille devices use the same raised dots, but bypass the hassle and expense of the paper printing process. Refreshable braille devices present a line of text at a time, and allow the user to feel it, then move on to the next line of text. 

The screen reader software to convert the digital text to braille is essentially the same as the screen reader software that converts digital text to speech, and allows for nearly identical functionality. It's just that the output is perceived through touch rather than through sound. For people who are both deaf and blind, tactile/touchable output is the only way for them to access web content at all.

## Why Perceivability Matters

If you can't perceive web content, it may as well not exist.

- If you can't see, all types of visual information—such as images, animations, colors, backgrounds, visual placement and layout—are completely useless, unless a digital text alternative is provided so that screen readers can convert that text into either sound or braille. The same is true in varying degrees for people with low vision or color-blindness.
- If you can't hear, audio content is completely unusable, and multimedia content—such as videos with sound—are much less useful than they could be, unless a text alternative is provided, in either caption or transcript format.

The good news is that you don't have to cure blindness or deafness to make images or sounds accessible to people with sensory disabilities. You just have to provide an acceptable alternative that works for their available sensory modalities.

To make an image accessible, provide a digital text description. Screen readers can convert this text description into speech or braille to make it available by sound or touch.

To make an audio recording accessible, provide a digital text transcript that deaf people can see with their eyes, and that people who are both deaf and blind can feel with their fingers when it is converted into braille.

Web accessibility can get more complicated than these simple examples, but the principles are still the same. Everything has to be perceivable to be at all useful.

## The Universal Format: Digital Text

You may have noticed that digital text solves the perceivability problem for people who are blind, for people who are deaf, and for people who are both blind and deaf.

Digital text is the most universally accessible format available, because it can be converted into all of the other useful sensory formats. That's something to make note of, and to keep in mind as you learn more about web accessibility.

Most digital text is visible on the screen, so it's easy to tell whether or not something is accessible at the most basic level of perceivability.

If you can see the text, and as long as it is real text and not just an image of text, chances are that screen readers can access it. (This is an oversimplification, because there are other factors that can interfere, but for simple web content this is generally true as a starting point.)

Sometimes, though, making all of the digital text visible on the screen is not the most appropriate technique. Sighted users can already see images, for example, so they don't need to see a text description of the image. It would be more appropriate to hide the image's text alternative from sighted users and make the text available only to blind screen reader users.

You can do this in HTML by hiding the text in the alt attribute of the img tag. Sighted users don't know it's there, but non-sighted users do, because their screen readers read it to them.

Similarly, people who can hear probably don't need to see the synchronized captions for video files or read the text transcripts for audio files, so it can be appropriate to allow users to turn captions on or off, and to provide links to full text transcripts rather than post all of the text in the middle of the web page for everyone to see.

And yet, if you want to make an image's description viewable by everyone, or if you want to make the captions or transcript viewable by everyone, that's OK too. There aren't any rules against it.

## Making Dynamic Content Perceivable

You can also make dynamic interactions accessible using digital text. You can use ARIA ("Accessible Rich Internet Applications") to announce when a tab is "expanded" or "collapsed". You can use an ARIA live region to announce new content as it is inserted into the DOM (Document Object Model).

There are lots of possibilities. And yes, you do need to announce these kinds of things. Blind users won't know when tabs expand or collapse unless this change of state is announced to them.

If new content is injected into a page—such as an error message or a confirmation message—blind users need to hear this new information. ARIA live regions can be used for this purpose, or you can move the browser's focus to those areas to force screen readers to read them. Either approach can be appropriate, depending on the circumstances and overall functionality of the interface.

## Make Sure Users Know What's on the Web Page

One way to summarize the need for perceivability is to say that users can't access content unless they know it's there. Make sure your users know what's on the web page.

This means making the content and functionality available through sight, sound, and touch.

Digital text—whether visible or hidden (using valid accessibility techniques)—is the most universal method of accomplishing the broadest perceivability.

## See Also

- The official Web Content Accessibility Guidelines, [Principle 1: Perceivability.](https://www.w3.org/TR/WCAG20/#perceivable)