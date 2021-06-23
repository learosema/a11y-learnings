# Visible Focus Indicator

## Overview

Sighted keyboard users need to be able to see where the keyboard focus is at all times. If they tab through a web page and they can't see where the focus is, website navigation becomes a guessing game. 

"I wonder what will happen if I press Enter now?" "How many times do I have to hit the tab key to get to the 'Contact us' link?" The website is basically unusable.

The good news is that you don't have to do anything to make the keyboard focus visible. Browsers take care of that for you. Some browsers (like Internet Explorer and Firefox) put a dotted outline around the active links and buttons. 

Other browsers (like Safari and Chrome) put a rounded solid outline around the active elements. As long as you don't do anything on purpose to turn off the browser's native focus indicator, you can meet the accessibility requirement for visual focus indicators.

## Don't turn off the focus outline

How does the visual focus indicator get turned off in the first place? It happens in the CSS

This breaks the keyboard usability of the website for sighted keyboard users:

```css
/* BAD */
a:focus {
    outline: 0; /* or outline: none; */
}
```

If you set the outline to 0 or to none, browsers suppress the native style and make it difficult or impossible for sighted users to navigate.

Some browsers display the URL in the bottom left of the screen, so users can see at least what the web address of the link is, but sometimes the URLs are indecipherable, with phrases like /index.aspx?rid=893248&session=23497hofaso829naa.

Nobody can make sense of that. Besides, not all browsers show the URL, so you can't count on users being able to see it at all.

## You can enhance the visual focus indicator

The native dotted outline in Internet Explorer and Firefox is good enough to pass the accessibility guidelines, but it's not always good enough for people with low vision, because the dotted line can be too small, or can appear with too little contrast.

You can customize the visual focus indicator by making it thicker, or by choosing colors that show higher contrast against the backgrounds on your site. When you customize it, you can choose any color combination that works for your site.

```css
/* BETTER */
a:focus {
    background-color: #fdf6e7;
    outline: 1px solid #8cc63f;
}
```

Sometimes you will need to create multiple color combinations for the visual focus styles, to accommodate different background colors in different sections of the site. The header might have a dark background, for example, and the content might have a light background.

You can create similar :focus styles for buttons and any other actionable elements.

## You can also enhance the hover and active states

Users with low vision will benefit from enhanced hover styles, because the enhanced styles will make it more obvious where the links are and whether the mouse is currently over a link or not.

```css
a:focus, a:hover, a:active {
    background-color: #fdf6e7;
    outline: 1px solid #8cc63f;
}
```