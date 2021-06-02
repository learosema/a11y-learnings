# Deafblind: A Tactile-Structural Text-only UX

## Overview

The experience on the web of people who are deafblind is very similar to the experience of people who are only blind. Both groups use screen readers. The difference is that a user who is blind listens to the screen reader, and a user who is deafblind feels the output of a screen reader to a refreshable braille device.

All of the web accessibility techniques for users who are blind apply to deafblind users, with the exception of the audio requirements (such as audio descriptions for videos), because deafblind users can't hear the audio. Interestingly, the techniques for deaf users don't apply well to deafblind users, because of the visual nature of the techniques, such as captions for videos. Deafblind users need everything in a machine-readable text format instead.

A refreshable braille device has little plastic pins that come up through small holes in the surface, forming braille characters. The user reads the line of text by moving a finger over the pins and feeling the characters. After reaching the end of the line, the user can press a button to read the next line, or the user can use various other button presses or keystrokes on the keyboard to navigate through elements on the page, essentially using the same techniques as blind screen reader users.

## Everything must be in a text format

In terms of the content of a web page, everything must be in a text format for deafblind users. Everything. No exceptions, but there are some nuances:

- The alt text for images counts as text.
- Labels, including invisible labels like aria-label count as text, as long as the elements are not hidden from screen readers via aria-hidden="true".
- ARIA live announcements, whether visible on screen or not, count as text.
It can be acceptable under some uncommon circumstances to add visually-hidden text just for screen reader users via the CSS clip method, but this method should be used only as a last resort.
- Synchronized captions in videos DO NOT count as text for the deafblind user, because, though some modern braille readers can display the captions, the captions change too quickly to read them in real time as a video plays. Also, there is no easy way to access the captions separately from the video, even if the captions are in a text format. A transcript is the only way that video or multimedia content can be made accessible to deafblind users.

## Multimedia for deafblind audiences

Basically, there is no such thing as multimedia for deafblind audiences. They can't see the video portion, and they can't hear the audio portion. The only thing you can really do with multimedia content is create an alternative text-based version, which usually means creating a transcript.

The transcript needs to be easy to find and should have a heading or some other kind of label to identify it as the transcript for the video. There are a few ways of posting a transcript on a web page:

- In regular paragraphs that everybody can access on the same page as the video.
  - If the transcript is long, you could set a height on the container and set it to overflow:auto, or similar, to allow sighted users to scroll through the transcript if they want. The scrolling aspect is irrelevant to users who are blind or deafblind, though. They will not even know there is a scrolling feature.
  - To provide a quick way for screen reader users to bypass the transcript, you could place a "skip transcript" link at the top of the transcript. You could either make this link visible at all times, or make it appear when it receives keyboard focus. You would NOT want to make the link invisible at all times to sighted users (e.g. using the CSS clip method), because that would confuse sighted keyboard users, who would not know where the keyboard focus is when it's on the hidden link. Using a hidden link would actually be fine for screen reader users (as long as you don't use display:none or visibility:hidden), but you have to take into account all use cases.
- In a dialog, available by activating a "Show transcript" button.
- On a separate page, available by activating a "Go to transcript" link.

There is no native way in HTML to programmatically associate a transcript to a video in the same way that you can associate captions with a video (e.g. using the `<track>` element), so even though it would be ideal to associate the transcript with the video, you really can't.

In theory, you could use aria-describedby on the `<video>` element to point to the transcript, but if the transcript is long, the screen reader would read the whole transcript when the focus lands on the `<video>` element.

That sounds like it might be a good idea, but it usually isn't, because when screen readers read aria-describedby text, they don't allow users to pause and restart from where it left off, or to navigate through the text. It all comes as a big text dump. If the user does pause the screen reader, the only way to hear the rest of the `aria-describedby` text would be to navigate away from the element, then navigate back to it, and listen to the `aria-describedby` text from the beginning again.

The imperfect solution to the problem of not being able to programmatically associate the transcript with the video is to place the transcript immediately after the video.

## The ideal design for deafblind users

The good news is that your main web design can be made perfectly accessible to deafblind users, without having to design a separate version, or doing too much extra work beyond what it takes to make things accessible to blind screen reader users. The most unique challenge for deafblindness is multimedia content.

### Think "text first"

Consider all multimedia content useless to this audience (though definitely not useless to other audiences!). For users who are deafblind, multimedia doesn't exist, so plan from the beginning to create text-based versions of all multimedia.

### Simplicity

As far as users who are deafblind are concerned, the simpler the design, the better.

### Semantic structure

Identify all the parts of the design and content with the proper semantic elements (landmarks, headings, links, form elements, etc.), and group things together logically so that they're easy to find.

### Control over timing

Using a refreshable braille device is generally a slower process than viewing the content with the eyes, and slower than listening to the content with a screen reader. Give users as much control over timing as possible, including being able to extend time limits and avoid session timeouts.

### Common wording

Many deafblind users will search in the page for keywords or phrases, so use wording that is common and expected. For example, users may want to find a "contact us" or "about us" page. If you use phrases like "get a hold of us" or "who we are," users won't find what they're looking for, even though those phrases are legitimate.

### Screen reader techniques

Apply all other screen reader accessibility techniques to the design, just as you would for users who are blind, because users who are deafblind benefit equally from them.
