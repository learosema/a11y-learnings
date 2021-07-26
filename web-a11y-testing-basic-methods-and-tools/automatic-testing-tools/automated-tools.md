# Automated Tools

## Overview

The range of capabilities of automated testing tools is broad. Basic tools test one page at a time using a defined set of rules. Some may even test for only one very narrowly defined type of error. At the other end of the spectrum, there are enterprise-level automated testing tools that use spiders to crawl and analyze multiple pages and have the ability to select a custom set of checking rules, record scripts, automatically fill out forms, schedule repeat tests, automate reports, and much more.

Outside of the enterprise-level tools, basic automated testing tools can be extensions or add-ons to a specific browser, while others are browser-independent. Mozilla Firefox and Google Chrome provide a number of helpful basic automated testing tools that take the form of add-ons or extensions that can be installed into your current browser with very little effort. We list, below, many of the tools that are available through Mozilla Firefox and Google Chrome as well as some browser-independent tools:

## axe DevTools Browser Extension for Mozilla Firefox and Google Chrome

The axe DevTools extension is a lightweight JavaScript library that allows testers and developers to assess content within the browser. This powerful tool uses accessibility rules that provide consistent results so that developers can apply fixes easily. The results also yield no false positives. It is one of the most robust free tools available today to run automated accessibility testing. This is the official tool Deque uses in its approach to testing and one we'll describe in greater detail on the next page.

Some of the key features include:

- Providing a comprehensive list of issues to fix in a single, detailed report
- Supporting color contrast analysis
- Interactive issue remediation
- Issue retesting
- [Information about axe DevTools Extension](http://www.deque.com/products/axe/)

## Tools for Mozilla Firefox

### Full Featured Firefox Accessibility Testing Tools

#### Firefox Web Developer Toolbar

This extension packs dozens of preconfigured tests that can help check for accessibility barriers.

- [Web Developer Toolbar for Mozilla Firefox](https://addons.mozilla.org/en-US/firefox/addon/web-developer/)

### Specialized Firefox Accessibility Testing Tools

#### Firefox Developer Tools

The formerly available Firebug extension, which was a general development and debugging tool, has been integrated directly into Firefox's native developer tools, which allow you to really focus on specific code snippets and analyze them. There is a wealth of development tools at your fingertips while you browse. You can edit, debug, and monitor CSS, HTML, and JavaScript live in any web page.

- Finding the Features Equivalent to Firebug's [Migrating from Firebug to the Firefox Developer Tools - Where to find features that were in Firebug](https://developer.mozilla.org/en-US/docs/Tools/Migrating_from_Firebug)

#### NoCoffee Vision Simulator

NoCoffee Vision Simulator is a Firefox extension tool that can be used to simulate various types of low vision conditions and to understand the issues people with low vision may have viewing a website. Some websites use colors that have low contrast and small text and target areas can potentially create barriers for people with low vision. Testers and developers can use the tool to help determine if text and colors on a web page are appropriate based on different types of low vision.

- [NoCoffee Vision Simulator for Mozilla Firefox](https://addons.mozilla.org/en-US/firefox/addon/nocoffee/)

## Tools for Google Chrome

### Accessibility Features in Chrome DevTools

The features of the now-deprecated Accessibility Developer Tools extension have been added to the built-in Chrome Developer Tools; this includes an Accessibility audit tab, and an Accessibility sidebar pane in the Elements tab.

### Web Developer Toolbar

The official port of the Web Developer extension from Firefox, this extension packs dozens of preconfigured tests that can help check for accessibility barriers.

- [Web Developer Toolbar for Google Chrome](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm)

### Firebug Lite for Google Chrome

Firebug Lite was the official port of the Firefox extension, and since it is not compatible with the latest versions of Chrome anymore, it has been forked and made available again by another author. Firebug Lite is not a substitute for Firebug or Chrome Developer Tools.

It is a tool to be used in conjunction with these tools. Firebug Lite provides the rich visual representation we are used to seeing in Firebug when it comes to HTML elements, DOM elements, and Box Model shading. It provides also some cool features like inspecting HTML elements with your mouse, and live editing CSS properties.

- [Firebug Lite for Google Chrome](https://chrome.google.com/webstore/detail/firebug-lite-for-google-c/ehemiojjcpldeipjhjkepfdaohajpbdo)

## Browser Independent Tools

These tools are not linked to a specific browser:

### Color Oracle

People who have colorblindness are sensitive to certain colors such as reds and greens. Color Oracle is one tool that can be used to test web page designs for effective color usage. Color Oracle is a free colorblindness simulator that can be used for Windows, Mac, or Linux. It applies a color filter on the web page that simulates how a person with colorblindness may see a design. Testers and designers can use the tool to determine whether colors used in the design may cause issues for people who have colorblindness.

- [Color Oracle](http://www.colororacle.org/)

### Colour Contrast Analyser

This is a great accessibility tool for when you need to do pixel picking to test color contrast ratios. It also simulates certain visual impairments, including colorblindness. The CCA is available for Windows and Mac, and in multiple languages including English, French, Dutch, Italian, German, Hindi, Korean and traditional Chinese.

- [Colour Contrast Analyser](https://www.paciellogroup.com/resources/contrastanalyser/)

### HTML_CodeSniffer

HTML_CodeSniffer is a client-side script that checks HTML source code and detects failures of a defined coding standard. HTML_CodeSniffer is written entirely in JavaScript, does not require any server-side processing and can be extended by developers to enforce custom coding standards by creating your own "sniffs". The bookmarklet has been designed to work with Google Chrome, Firefox 10+, Safari 5+ and Internet Explorer 8+

- [HTML_CodeSniffer](http://squizlabs.github.io/HTML_CodeSniffer/)

### WAVE

WAVE is a free online service that evaluates for accessibility by offering visual representations of a webpage’s accessibility issues. It's also available in Firefox and Chrome extensions and as an API.

- [WAVE](http://wave.webaim.org/)

### Other Tools

#### Xcode Accessibility Inspector (Mac)

The Accessibility Inspector available through the Xcode app on a Mac allows developers to test web applications for accessibility. The tool lets developers see how a screen reader, VoiceOver in particular, may interact with controls and other interface elements on a web page.

Developers can analyze the accessibility information of their apps with the tool, such as the label, value, and traits for each control. It is common to use the tool in conjunction with VoiceOver to test and debug pages and apps for accessibility issues.

- [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)
- [Testing for Accessibility on OS X](https://developer.apple.com/library/mac/documentation/Accessibility/Conceptual/AccessibilityMacOSX/OSXAXTestingApps.html)

#### Accessibility Viewer (Windows)

The Accessibility Viewer (aViewer), developed by The Paciello Group, is a free, open source inspection tool that allows testers and developers to easily access the Accessibility API information generated by browsers and assistive technologies like screen readers. Similar to the Xcode Accessibility Inspector, developers can use the tool to test and debug accessibility issues of web applications.

- [Accessibility Viewer (aViewer)](https://www.paciellogroup.com/resources/aviewer/)
