# Video and Audio Alt Text, Transcript, Captions, Audio Descriptions

## There is no alt attribute for video and audio

The alt attribute is not allowed on `<video>` or `<audio>` elements to add alternative text to videos, but there are other ways of making video content accessible:

- Synchronized captions
- Text transcript
- Audio descriptions


## All prerecorded video MUST have synchronized captions.

Captions make the dialog and narration accessible to deaf audiences. The captions must include all of the dialog and narration. The captions must also identify who is speaking, to eliminate any possible confusion. 

If there are other important sounds — such as applause, laughter, etc. — the caption should indicate those sounds, either in brackets or in parentheses.

The greatest amount of user-defined flexibility in captions can be achieved with [WebVTT](https://w3c.github.io/webvtt/) (the Web Video Text Tracks Format).

Some browsers, such as Safari on OS X and on iOS, allow users to define their captioning preferences at the operating system level. They can set font size, color, background color, and typeface.

Every time a video plays with WebVTT captions, the video player will honor the person's preferences. Storing the caption preferences in a centralized location in the operating system is convenient for the users, who won't have to choose settings every time they watch a new video.

## Prerecorded audio content MAY have synchronized captions.

Prerecorded audio-only content can be captioned too, though in most cases a text transcript will suffice.

## All live video with dialog and/or narration MUST have synchronized captions.

Live videos MUST have synchronized live captions. Live captioning requires a professional stenographer — a person who uses a stenograph machine to type the spoken content — and a live text feed that accompanies the video. 

A stenograph machine is similar to a computer keyboard in concept, but it has fewer keys and allows the trained stenographer to type in syllables or sounds, rather than only in individual letters.

## Live audio consisting mainly of dialog and/or narration SHOULD have synchronized captions.

If the live audio content contains dialog and/or narration, it is usually appropriate — and may in fact be necessary — to provide live synchronized captions. 

If the live audio content contains music or other similar types of sounds, live captions may not be necessary, and may not be meaningful, but it depends on the context. 

Live streaming of text descriptions can be useful even for things like music concerts, to give deaf audiences a sense of the event itself, in real time. 

In some cases, posting a text transcript or description of the event after the event has concluded may be acceptable, and is a bit of a judgment call.

## All prerecorded video and audio MUST have text transcripts.

People who are both deaf and blind can neither hear nor see video or audio content. The only solution for deafblind users is a text transcript, which they would read via a refreshable braille output device. 

A refreshable braille output device is hardware that has a row of holes, allowing small plastic pins to poke through and form braille characters. The person reads the braille characters with the finger, then presses a button to proceed to the next line of text. The pins reconfigure into the braille characters for the new line of text.

A text transcript is essentially a text log of all of the dialog and narration in a video, similar to the captions, but available separately from the video itself. As with captions, the text transcript should identify who is speaking, plus note sounds like applause and laughter.

It should also describe other visual information — for example, descriptions of scenery, non-verbal communication between people, and anything else to provide an equivalent alternative to the content for people who are deafblind.

The transcript can be presented on the web page itself (usually below the video), or on a separate web page (with a link from the video page), or in a popup dialog, or even in a separate document (e.g., a text file or MS Word document).

## Videos MUST include audio descriptions of important visual content that is not conveyed through the audio.

If a video has visual elements that aren't conveyed through the audio — such as important facial expressions, hand gestures, text shown on the screen, visual action sequences, etc. — blind audiences may not be able to understand what is happening unless someone describes the visual components to them.

That’s where audio descriptions can help. Audio descriptions are an audio track played simultaneously with the original video, with a narrator describing the important visual information to blind users.
