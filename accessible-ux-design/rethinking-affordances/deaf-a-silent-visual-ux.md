# Deaf: A silent visual UX

## Multimedia

The main accessibility challenge with audiences that are deaf is video and audio content. The vast majority of videos on the web are not captioned, making them inaccessible to those who can't hear the audio. The solution is straightforward: provide synchronized captions. 

The module in this series on Audio, Video, Animations, and Motion covers captioning guidelines and techniques in detail. There are a few highlights from those materials worth mentioning:

### Provide the captions as separate synchronized files

Don't embed the captions in the video (i.e. as open captions always visible to everyone), in most circumstances. It's usually best to provide the captions as separate caption files, synchronized with the video. It's not wrong to put the captions in the video — and in fact it can be a good thing to do if you're trying to prove a point about how important captions are — but there is more flexibility for users when the captions are separate from the video. They can turn the captions on or off and, depending on how things are set up, they may be able to also adjust colors, size, and font.
### Provide captions in multiple formats

To accommodate as many browsers as possible, provide captions in several caption formats.

### Provide WebVTT captions

One of the most versatile caption formats is WebVTT, because users can set their preferences for colors, size, and font at the operating system level, and browsers that support WebVTT customization will honor those settings across all videos that the user plays.

### Provide caption customization options in the media player

Not all browsers support WebVTT customization, so give users the option to customize the caption settings in the media player itself. Make the settings easy to find and adjust. The most important options are text color, background color, text size, and font. You could also have options for caption placement (above video, below video, overlaid over the video, etc.). Important: If possible, save the user's caption preferences, so they don't have to keep adjusting the settings on every video.

### Live events

Live events require captions. Live captions require a professional transcriber. In theory, a very good speech recognition system could also perform that task, but unless the quality of the audio is well-controlled, an automated system isn't going to be good enough.

There are two main ways to provide captions for live events:

1. Use a professional broadcast system to embed the captions in the video itself in real time.
2. Use AJAX to provide synchronized captions with a live video. This option can be tricky to set up. The live captions will never be fully synchronized with the live video, because of the delay involved in transcribing the words. One way to get around this is to experiment with a delay in the video feed. Depending on the speed of the transcriber and other variables, you may want to delay the video by 10 to 30 seconds to try to achieve captions that are nearly synchronous with the video. The captions could be displayed within the media player itself, or directly below the media player.

## Sign language

For many people who are deaf, sign language is their first language, and may still be their most fluent language. Having content in sign language is more useful than text content to some people who are deaf. This is particularly true for video content. Captions appear and disappear from the screen quickly and may not provide enough time for people to read them if written language comprehension is not one of their strengths.

There are a few ways to provide sign language interpretation for videos:

- Include a sign language interpreter in the original video, standing or sitting next to the speaker.
- Use picture-in-picture (PiP) technology to show the sign language interpreter in a corner of the video, or off to the side.
- Allow the user to turn the sign language interpretation on or off, and play the interpretation as a separate video next to the original video, synchronized with the original video.

## Opportunities to innovate for users who are deaf

Here are a few ideas for projects that could make a difference for users who are deaf:

### Automated captioning via speech-to-text technology

Automated captioning will be useful when automated speech-to-text recognition is mature. The technology is respectable already, but still not accurate enough in many situations. Improvements to text-to-speech software will open up a world of possibilities for people who are deaf. Outside of web accessibility, imagine the impact of a mobile app that a person who is deaf can use to interpret daily conversations from spoken language into text. The person could respond via text or, even better, through sign-language-to-text or sign-language-to-speech technology.

### Text-to-sign language conversion

Improve language translation software for converting written text to avatar-based sign language. The conversion is a true language conversion, because sign languages are not simply verbatim versions of oral languages. American Sign Language (ASL), for example, is based somewhat on French grammar, but it still has its own unique syntax.

### Sign language recognition

Converting signs by a human into text is a much more difficult challenge than text to sign language, but having that kind of technology would be extremely useful, particularly in the case of people whose most fluent language is sign language.

### Add sign language options to media players

Most media players do not have the option to turn on sign language interpretation. Even when sign language interpretation is available, most media players do not support a separate sign language track, so the sign language must be permanently added to the original video, or to a copy of the video. 

Producing separate versions of the original video is not a problem for users, but it can be problematic in terms of video production, especially if you don't own the video copyright. Creating a media player with a sign language option allows you to create a separate video of just the sign language interpretation. 

That video can be positioned over part of the main video, or to the side of the video, or above or below it. It can be made as large as necessary to make the sign language easy to understand, and you don't have to touch the original video at all.

### Innovate ways to make adding sign language more cost-effective

Adding sign language to videos is time-consuming and potentially costly. There isn't a ready-made solution to lowering the time investment required to produce sign language videos — and it's probably not a good idea to undercut the work of sign language interpreters by pressuring them to work at a reduced rate or for free — but there are probably ways to increase the availability of videos with sign language interpretation from a business or entrepreneurial perspective.
