# Automated solutions

The fantasy accessibility solution that we all would love to have is an automated feature that would take inaccessible content and magically convert into accessible content. How realistic is this fantasy? The good news is that significant progress has been made in some areas. The bad news is that we still have a long way to go in other areas, and it will never be fully possible without being able to read the mind of the author, because some accessibility features depend on intent, not just on technical methods.

## Skype Translator

Skype Translator was originally designed to help people talk across languages. The voice recognition software converts the speech to text, then the text is converted from one language into another. It wasn't until later that the potential to help deaf users was fully realized. This application now allows people who are deaf to communicate in real time with hearing people.

Watch the [video about Skype's feature for people who are deaf](https://www.youtube.com/watch?v=spqqcJf5e5Q)

## Automatic captions on YouTube videos

Automatic captioning has been available on YouTube for years, by running voice recognition algorithms on the audio track of the video, and then synchronizing the result with the video. The technology has been steadily increasing in quality, to the point that some videos have exceptionally high automatic caption accuracy rates, but only under certain conditions:

- The voice (narration and/or dialog) must be clear.
- The overall sound quality must be good.
- There must not be overlapping voices.
- There must not be significant interference from background sounds or music.
- The speakers' accents must be familiar to the YouTube algorithms.

Despite the inaccuracies, automatic caption technology holds a lot of promise. If the algorithms can get as good as humans at deciphering bad quality audio or overlapping voices, essentially every video on the web can potentially be captioned well enough for people who are deaf to get everything they need out of the videos, without content authors having to do any work at all. We're not there yet, but we're headed in that direction.

## Audio descriptions

Automatic captions don't solve everything. Videos still need audio descriptions for the benefit of people who are blind. Audio descriptions are narrated descriptions of the visual aspects of videos that can't be understood by listening to the audio alone. Examples include: words written on a chalkboard which aren't read out loud, important facial expressions, physical actions (like throwing a ball or dancing), etc. It's hard to imagine an auto-audio-description feature that would actually work or be useful, but maybe after several years of experimentation with artificial intelligence, it might be possible.

## Automated alt text on Facebook images

In April of 2016, Facebook announced that it has begun automatically adding alt text to images under some circumstances. They rolled out the feature first on the iOS platform, then on the regular web site and on Android. Refer to the [Facebook press release and video about automatic alt text](http://newsroom.fb.com/news/2016/04/using-artificial-intelligence-to-help-blind-people-see-facebook/) for details about the announcement.

The feature is surprisingly good, within limitations. Facebook has erred on the side of being conservative in how much to say or guess about an image, and prefaces each description with the phrase "Image may contain."

## The inherent limitations of automated alt text

As the above examples demonstrate, Facebook's algorithms are quite sophisticated, yet they still do not convey a full description of the image, in the literal sense of describing what is in the image. More importantly, though, there is no such thing as one right alt text for images.

- If the purpose of the apple and orange image is to illustrate the specific varieties of apples available at a store (Fuji, granny Smith, etc.), the alt text would need to convey that purpose. The oranges, in that case, are irrelevant, and would not even need to be mentioned.
- The same image could be used as a way to say "Hey look what I bought at the store today: fruit! I'm trying to eat more healthily, and this is proof!" If that's the case, then the types of apples are irrelevant, but the fact that there is a lot of fruit (and no fatty foods) is what the alt text would need to convey

Even so, even limited, non-specific alt text can be better than no alt text at all.

### Missing: The ability to add custom alt text to cover images

There is currently no way to add custom alt text to a cover image in Facebook. That's a serious oversight. It wouldn't take much to add an alt text field to the image upload/edit interface. 

Facebook does allow image descriptions, which are visible on the screen, which can potentially serve the same purpose, but the description field is rarely used that way. The good news is that Facebook does allow custom alt text to a photo within a post, though the method to add it isn't obvious.

#### Inadequate image description examples

- "Look what I bought!"

## The future of automated accessibility solutions

Beyond voice recognition for chats and videos or automated alt text, where else might we see automated accessibility solutions? Here are a few ideas:

- Automated table structure: Software that recognizes table structure even when the table is not marked up appropriately, and can apply table headers where necessary.
- Automated form labeling: JAWS and VoiceOver already make intelligent guesses about the labels for form fields that don't have labels. This logic could be extended and improved.
- Automated ARIA widget correction: Software could recognize what type of widget the author meant to create, then fix it.
- Automated contrast correction: Algorithms could adjust the contrast on the fly, or post warnings during the authoring process.
- and so on...

It's important to note that automated solutions can be applied in at least two main places:

- During the authoring process
- On the end result

Facebook could add the alt text to an image, then prompt the author: "Is this good alt text? If not, please write a more accurate image description." That would put the sense of responsibility back on content authors, where it belongs.


