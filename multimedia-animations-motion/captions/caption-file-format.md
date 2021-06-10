# Caption File Format

## Multiple caption file formats SHOULD be provided.

A caption file contains all of the spoken words and descriptions conveyed through a video and audio presentation as well as the time codes for when the captions should appear when the video is played.

Media players support different types of caption files, so it is important to know which files your platform or player supports. Most players support the basic SubRip caption file with the file extension .srt. But there are a growing number of players that support advanced caption files like WebVTT (file extension .vtt).

While basic file formats generally require only the time codes, advanced file formats allow for more flexibility in the styling and positioning of captions. It is important, though, to not rely on only one caption file format. 

Including file formats that are both basic and advanced will help to ensure that your captions are published and viewed by the largest audience possible; and including advanced file formats may allow users to customize the look of captions based on their preferences.

### Basic caption file formats include the following:

- [SubRip (.srt)](https://en.wikipedia.org/wiki/SubRip#SubRip_text_file_format)
- [SubViewer (.sbv or .sub)](https://wiki.videolan.org/SubViewer)
- [LRC (.lrc)](https://en.wikipedia.org/wiki/LRC_%28file_format%29)

### Advanced caption file formats include:

- [WebVTT (.vtt)](https://w3c.github.io/webvtt/)
- [SAMI (.smi or .sami)](https://msdn.microsoft.com/en-us/library/windows/desktop/dd562301%28v=vs.85%29.aspx)
- [TTML (.ttml)](https://www.w3.org/TR/ttaf1-dfxp/)


## At least one of the file formats SHOULD be in a WebVTT file format.

WebVTT is one of the most useful formats for web captions because users can set it in the operating system and the settings will be consistent across all WebVTT videos in browsers that support WebVTT. Browsers that support WebVTT and caption customization include Safari on macOS and iOS. 

So, when creating caption files, be sure to include WebVTT as one of the file formats to allow users to modify captions based on their preferences.

