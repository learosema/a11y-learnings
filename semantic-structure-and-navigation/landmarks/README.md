# Landmarks

## Introduction

Despite all of the talk about using correct semantic structure for accessibility, HTML has historically lacked some key semantic markers, such as the ability to designate sections of the page as the header, navigation, main content, and footer. With HTML 5, these designations are possible, using the new elements `<header>`, `<nav>`, `<main>`, and `<footer>`. Similar functionality is available using the ARIA (Accessible Rich Internet Application) attributes role="banner", role="navigation", role="main" and role="contentinfo".

JAWS, NVDA, and VoiceOver support the ability to navigate to sections of a web page using ARIA landmarks. This is a more elegant solution to the problem of providing a way for users to skip to the main content of the web page. There is no visible alteration to the web design, making it unobtrusive and invisible. Of course, the fact that this technique is invisible is fine for blind screen reader users, but not so fine for sighted keyboard users or screen enlarger users with low vision. In this sense, HTML 5 regions and ARIA landmarks cannot yet replace the old-fashioned "skip navigation" links. Browsers still do not have a built-in way to notify users that HTML 5 regions or ARIA landmarks are present. Screen reader users are the only ones who can take advantage of them. There is a Firefox ARIA landmark extension available, which adds the ability to navigate by landmarks in Firefox, but this is not a native feature of the browser.

## In this Section:

- [Creating Landmarks (HTML5, ARIA)](creating-landmarks.md)
- [Best Practices for Landmarks](best-practices-for-landmarks.md)
- [Backward Compatibility](backward-compatibility.md)
- [Navigating Landmarks with Screen Readers](navigating-landmarks-with-screen-readers.md)
