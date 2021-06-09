# Windows High Contrast Mode

## Using Windows High Contrast Mode

There are multiple ways to turn on Windows High Contrast Mode on Windows 10. To open the settings for Windows High Contrast Mode, you can:

- Either type in "high contrast settings" in the search field of the taskbar
- Or [Win] + [U] -> high contrast

Once you have applied a theme to your computer, you can quick-toggle it via [left Alt] + [left Shift] + [Print Screen].

## High Contrast Themes

In Windows, there are four preset high contrast themes: High Contrast #1, High Contrast #2, High Contrast Black, and High Contrast White. The High Contrast Black theme features a black background, white text, yellow links, bright green disabled text, and highlights selected text in turquoise and black text.

High Contrast White uses a white background, black text, blue hyperlinks, maroon disabled text, and highlights selected text using dark blue background and white text. High Contrast #1 and #2 themes are variations of the High Contrast Black theme.

All of the themes can be customized by users based on their preferences; but for testing, the preset themes can be used. In fact, it is best to test with at least one high contrast black theme and one high contrast white theme as text, links, icons, and other elements can appear very differently in each theme.

## Browser Settings

Depending on the browser you are using, you may or may not see a web page display using the high contrast theme. You can change whether your browser uses the system's high contrast theme under the browser's options. This setting may be the default for some browsers, but you may need to enable this option in other browsers.

### Common Windows Browsers and High Contrast Settings

- Edge: Automatically uses system's high contrast theme
- Internet Explorer: Default is to use system's high contrast theme. Options can be found under Tools > Internet Options > General tab > Colors (Under Appearance on the General tab) > Check or Uncheck Use Windows Colors
- Firefox: Open Menu > Options > Content > Colors... (Under Fonts & Colors) > Select Use systems colors in the dialog box
- Chrome: Will detect that you are using a high contrast theme on the computer 

## Web content MUST retain all essential visual information in Windows High Contrast Mode.

People who have low vision or other types of visual disabilities may utilize high contrast settings like Windows High Contrast Mode to read and interact with web pages. 

Windows High Contrast Mode overrides the original colors according to user preferences. When high contrast mode is enabled, though, it is important to keep in mind how the high contrast settings affect the original styles of a web page.

You should consider how the styling of a web page will appear to users who benefit from using high contrast settings. Use real text whenever possible, as images of text cannot be customized and text used in background images may be completely hidden from the user.

Informative images in the background may also be hidden, so be sure to not place them on the page using CSS. Also, do not rely on color alone to communicate information since high contrast settings may override colors on a web page.

The CSS styles of a web page should not prevent how a user reads and interprets content when high contrast settings are enabled.

## The design MUST NOT override Windows High Contrast Mode.

The Microsoft-specific `-ms-high-contrast` media feature and `-ms-high-contrast-adjust` CSS property can override user's high contrast themes in Internet Explorer. However, the CSS property and media queries should never be used as they don't allow the user to customize a page based on his or her preferences.

