# Overall page UX

## Screen readers create an audio-structural experience

People who are blind use screen readers to listen to the content. It is a synthesized voice that converts text to speech. It is possible to go to a web page and let the screen reader read the whole page out loud, from start to finish, but hardly anyone ever does that.

If you did that, you'd have to listen to all of the content at the top of the page every time — including the brand, the main navigation (which might contain many links), and other features like search, login, etc. — before arriving at the main content.

Once you arrive at the main content, you'd have to listen to all of it. You couldn't skim through the less interesting parts. And then you'd have to listen to all of the links and information in the footer.

It would be a waste of time to listen to everything on every web page every time.

Not only that, but you if you're going to interact with the web page in any way — like fill out and submit a form, or expand a collapsed menu, or click on a link — you're going to have to pause the screen reader and use the keyboard to perform the relevant tasks.

As a blind user, how do you know when you come to a link, or to a text input, or to a button? The answer is that the screen reader tells you (it says "link" or "text input" or "button" when reading the elements). The screen reader knows what the elements are because of how they are represented by the accessibility API of the browser and the operating system.

### Example: semantic structure of the Wikipedia home page

- Landmarks (0 total)
- Headings (1 total)
  - Level 1: "Wikipedia The Free Encyclopedia"
- Form elements (4 total)
  - Text input: "Search"
  - Select list: "English"
  - Button: no label is provided
  - Button: Read Wikipedia in your language
- Images (2 total)
  - "Wikipedia"
  - "Wikipedia logo"
- Links (11 total, in this part of the page)
- Lists (0 total, in this part of the page)

#### Issues

- no landmarks on the page. Most useful are `header`, `nav`, `main` and `footer`
- the search button has no label
- links: The link text includes both the name of the language (e.g. English), and the number of articles (5,323,000+). Unfortunately, the numbers are written with spaces in the middle of them instead of commas (in American notation) or periods (as in most other areas of the world). The spaces divide the number. Instead of saying "five million, three hundred and twenty-three thousand" as it should, it actually says "five, three hundred twenty-three, zero zero zero." Trying to be fancy with the numeric notation breaks the correct pronunciation of the numbers for screen reader users.
- lists: no lists. The list of languages near the top of the page could be styled as list items. If it were styled as a list, the screen reader would say "list with ten items," which helps the user understand the amount of content within the list. 

### Example: A Wikipedia article page

The audio-structural experience on an article page in Wikipedia is different from the experience on the Wikipedia home page because the semantic structure is quite different. The page is the Wikipedia article on web accessibility opens in a new window. This time we'll show the overall audio-structural view first:

#### The Audio-structural "view" of a Wikipedia article
- Landmarks (13 total)
  - Main landmark
  - Navigation landmark: "Personal tools"
  - Navigation landmark: "Namespaces"
  - Navigation landmark: "Views"
  - Search landmark
  - Banner (header) landmark
  - Navigation landmark: "Navigation"
  - Navigation landmark: "Tools"
  - Navigation landmark: "Interaction"
  - Navigation landmark: "Print/export"
  - Navigation landmark: "Other projects"
  - Navigation landmark: "Languages"
  - Content Info (footer) landmark
- Headings (43 total)
  - Level 1: "Web Accessibility"
  - Level 2: "Contents "
  - Level 2: "Assistive technologies used for web browsing [ edit ]"
  - Level 2: "Guidelines on accessible web design [ edit ]"
  - Level 3: "Web Content Accessibility Guidelines [ edit ]"
  - Level 3: "Criticism of WAI guidelines [ edit ]"
  - Level 3: "Other guidelines [ edit ]"
  - Level 4: "Canada [ edit ]"
  - Level 4: "Philippines [ edit ]"
  - Level 4: "Spain [ edit ]"
  - Level 4: "Sweden [ edit ]"
  - Level 4: "United Kingdom [ edit ]"
  - Level 4: "Japan [ edit ]"
  - Level 2: "Essential components of web accessibility [ edit ]"
  - Level 2: "Guidelines for different components [ edit ]"
  - Level 3: "Authoring Tool Accessibility Guidelines (ATAG) [ edit ]"
  - Level 3: "Web Content Accessibility Guidelines (WCAG) [ edit ]"
  - Level 3: "User Agent Accessibility Guidelines (UAAG) [ edit ]"
  - Level 2: "Web accessibility legislation [ edit ]"
  - Level 3: "Australia [ edit ]"
  - Level 3: "Brazil [ edit ]"
  - Level 3: "European Union [ edit ]"
  - Level 3: "Ireland [ edit ]"
  - Level 3: "Israel [ edit ]"
  - Level 3: "Italy [ edit ]" (and more...)
- Form elements (4 total)
  - Button: "hide"
  - Search text field: "Search Wikipedia"
  - Button: "Go"
  - Button: "Language settings
- Images (4 total)
  - "Handicapped accessible sign.svg"
  - "Category"
  - "Wikimedia Foundation"
  - "Powered by MediaWiki"
- Links (441 total)

Lists (41 total top-level lists: 39 bulleted lists and 2 numbered lists; 53 total lists including sub-lists)

Can you get a sense of what is on the page from this audio-structural view? This is the main view of the page from a screen reader perspective. All of the other visual aspects are irrelevant to screen reader users. The more you can think in terms of the semantic structure, the more successful you will be at creating a good user experience for screen reader users.

#### An audio-structural analysis of the Wikipedia article page

<b>Landmarks</b>: In contrast to the Wikipedia home page, the design for Wikipedia article pages has many landmarks:

- a main landmark (`<main>` or `<div role="main">`)
- 9 navigation landmarks (`<nav>` or `<div role="nav">`), each with names to allow users to distinguish them from each other.
- a search landmark (`<div role="search">`)
- a banner/header landmark (`<header>` or `<div role="banner">`)
- a footer/contentinfo landmark (`<footer>` or `<div role="contentinfo">`).

The list of available landmarks is pretty good, though 9 navigation landmarks is a bit excessive. It's usually best to keep the number of landmarks to a relatively short list, because part of the point of landmarks is to make it faster and easier to find things. The more landmarks there are, the less they help make things faster or easier.

<b>Headings</b>: The heading structure is very good. There are a few headings in the template, followed by a good hierarchical structure in the article itself, with a few headings in the footer. The one thing that is perhaps a little confusing is the "[ edit ]" at the end of the headings in the main article. That is a link which allows people to edit the text in that section of content. The link is in the heading itself. That's not a problem, really. It just takes a little getting used to.

<b>Form elements</b>: The form elements have acceptable labels.

<b>Images</b>: The first image in the list is a file name ("Handicapped accessible sign.svg"), which means that the image does not have alt text. Screen readers will typically use the file name when alt text is not available. In this particular case, we got lucky: the file name happens to be human-readable and easily understandable. But if the file name had been something like `img0298.svg`, we would have no idea what the image is trying to convey.

<b>Links</b>: The list of links is extremely long. That's not a problem. One thing that is a problem, though, is several of the links have the exact same text: "[show]". When navigating the list of links like this, it's impossible to distinguish those links from each other.

<b>Lists</b>: There are a lot of lists on this page, many of which are sub-lists in a hierarchy. Some of them are navigation-related. Others are in the content. The fact that they are marked as real lists (`<ul>` and `<ol>`) is a good thing.

## What is the ideal audio-structural user experience for a page?

How should you approach the task of designing a good audio-structural user experience? Is there such a thing as an ideal audio-structural UX?

Every web site is different, and every page design is different, but there are some things to keep in mind as a starting point.

### Ideal landmarks

A theoretical list of ideal landmarks might look something like this:

- `<header>` (or `<div role="banner">`)
- `<nav>` (or `<div role="navigation">`)
- `<div role="search">`
- `<main>` (or `<div role="main">`)
- `<footer>` (or `<div role="contentinfo">`)

That's all you really need. It's a rather short list of landmarks, and that's a good thing. Keep in mind that the purpose of landmarks is to make it easy to find parts of a web page and to save the users some time. If the list of landmarks is too long, the users will spend as much time hunting for things in the landmarks as they would hunting for things in the page itself.

In most cases, you want only one header, one search, one main, and one footer. You can have multiple navigation regions, but it's often best to limit it just to the main navigation. If you do designate multiple navigation regions, give them unique names using aria-label (e.g. `<nav aria-label="Product categories">`)

### Ideal headings

The ideal heading structure starts with a heading level 1 (`<h1>`) inside of the main content (`<main>` or `<div role="main">`).

There ought to be only one heading level 1, if possible, though this is not an absolute rule. A dialog should also start with a heading level 1, because a dialog is essentially a stand-alone view, almost like a mini web page.
Each major section of content should be represented by a heading.

The heading levels should form a logical hierarchical outline of the content on the page.
Headings should not skip levels (a child element of a heading level 2 should be a heading level 3, for example, not a heading level 5).

### Ideal form elements

From a semantic perspective, the most important thing is that all form elements need accurate labels (`<label>`). There are many other aspects of form accessibility, but the other techniques come into play when interacting with the form, rather than when listing form elements.

### Ideal images

The alt text will show up in the list of images, so you want to first make sure the image has alt text, and second make sure the alt text quality is good. It needs to be accurate, succinct, and meaningfully descriptive of the image's purpose.

### Ideal links

The most important thing is that every link needs to have a valid accessible name. The accessible name can consist of regular text, the alt text of an image within the link, or a label (via aria-label or aria-labelledby).

The link text should also adequately convey the purpose or destination of the link.

If possible, the link text should make sense when taken out of context and should be unique so that users can distinguish between links when listing all of the links on the page.

Put in as many links as you need. Wikipedia article pages tend to have more links than average web pages, but the links are appropriate, and it's not wrong to have a lot of links, though admittedly it will take a long time to navigate through them all.

### Ideal lists

The key is to use actual list markup (`<ul>`, `<ol>`, or `<dl>`) whenever presenting a list.
Also, be sure to use the right type of list for each circumstance.
Use as many lists as you need.

