# Leveraging Authoring tool Accessibility guidelines

##  Overview
A lot of developers don't think of their web applications as authoring tools even when they have authoring capabilities built into them. 

If the developers are aware of accessibility, they think of the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG20/), and may not have even heard of the [Authoring Tool Accessibility Guidelines (ATAG)](https://www.w3.org/TR/ATAG20/), let alone think those guidelines apply. But they do apply, if your application allows user input that can be posted on the web. Examples include:

- Content management systems and blog authoring systems
- User comment features (forums, discussions, blog comments, etc.)
- Product rating and review features
- Social media platforms
- Document review and collaboration features
- Anything that invites and posts user input

Overall, ATAG 2.0 is divided into two sections:

1. Make the authoring tool user interface accessible.
2. Support the production of accessible content.

To a large degree, the section about making the authoring tool user interface accessible is a summary of important points in WCAG 2.0, so we won't analyze that section here. Instead, we'll discuss the points about supporting the production of accessible content.

## Fully automatic processes produce accessible content ([ATAG B.1](https://www.w3.org/TR/ATAG20/#principle_b1))

### Ensure that automatically-specified content is accessible ([ATAG B.1.1](https://www.w3.org/TR/ATAG20/#gl_b11))

Build a library of accessible templates and methods that is already accessible, so that users don't have to worry about the accessibility of the output if they use those pre-made templates and methods. Thoroughly vet them for accessibility so that there is nothing to fix when authors use them.

### Ensure that accessibility information is preserved ([ATAG B.1.2](https://www.w3.org/TR/ATAG20/#gl_b12))

Be careful that your content filters don't erase accessibility features that the authors may have added in themselves. Either be less stringent about the content or add intelligent algorithms that recognize and preserve accessibility features. 

The first option is easier, by far, but might cause some security concerns. The second option is much more work, but potentially safer.

## Authors are supported in producing accessible content ([ATAG B.2](https://www.w3.org/TR/ATAG20/#principle_b2))

### Ensure that accessible content production is possible ([ATAG B.2.1](https://www.w3.org/TR/ATAG20/#gl_b21))

There are two main approaches to fulfilling this guideline:

- Create authoring widgets that have a full set of built-in accessibility features.
- Allow authors to customize the output (e.g. edit the HTML source).

Allowing authors to edit the HTML source is a great fallback for all situations, but realistically you can't expect hardly anyone to use it if the majority of the authors are non-technical. You have to build in accessibility features into the authoring widgets themselves. Here are some examples:

- A widget for adding images that allows users to specify alt text.
- A widget for creating HTML tables that allows users to specify a `<caption>`, table headers, and the scope for those headers.
- A widget that allows users to specify headings (and ensure the resulting code is actual headings, not paragraphs or `<div>` elements styled to look like headings).


### Guide authors to produce accessible content ([ATAG B.2.2](https://www.w3.org/TR/ATAG20/#gl_b22))

If we use the example of a widget for creating HTML tables, the methods for specifying a `<caption>`, table headers, and the scope for those headers ought to be easy to find and use. 

The visual interface could include a graphic representation of a table, showing where these features would go. It can include text instructions explaining what the features are and why they're important. It could include a wizard-like interface to guide them, step-by-step through the process. There are many ways to approach this.

### Assist authors with managing alternative content for non-text content ([ATAG B.2.3](https://www.w3.org/TR/ATAG20/#gl_b23))

For starters, authors should be able to add alt text to a single image for one use. But you can do more than that. Images and media that might be reused in multiple places should have accessibility attributes that can also be reused.

The alt text of an image in an image library or collection should remain associated with that image. Authors should be able to insert the image with the existing alt text left intact. You can also give them the option of editing the alt text to better fit the new context, without altering the original alt text in the image library.

### Assist authors with accessible templates ([ATAG B.2.4](https://www.w3.org/TR/ATAG20/#gl_b24))

- Have ready-made accessible templates that authors can use.
- Allow authors to create their own reusable accessible templates, prompting them along the way on key accessibility features.
- Warn users about any inaccessible pre-authored templates in the system, and encourage them to use the accessible templates.

### Assist authors with accessible pre-authored content ([ATAG B.2.5](https://www.w3.org/TR/ATAG20/#gl_b26))

The same ideas apply to content as to templates (above):

- Have ready-made accessible content that authors can use.
- Allow authors to create their own reusable accessible content, prompting them along the way on key accessibility features.
- Warn users about any inaccessible pre-authored content in the system, and encourage them to use the accessible content.

## Authors are supported in improving the accessibility of existing content ([ATAG B.3](https://www.w3.org/TR/ATAG20/#principle_b3))

This category refers to creating tools that help authors fix content retroactively, after it has been created.

### Assist authors in checking for accessibility problems ([ATAG B.3.1](https://www.w3.org/TR/ATAG20/#gl_b31))

An authoring tool can provide a utility like an "accessibility checker" to run an audit on existing content to find accessibility errors. Any auditing tool of that kind will have limitations. It cannot substitute for a review by a knowledgeable human being, but at least it can find some kinds of errors and can be especially helpful for newcomers to accessibility.

### Assist authors in repairing accessibility problems ([ATAG B.3.2](https://www.w3.org/TR/ATAG20/#gl_b32))

Assisting users with repairs can be accomplished by:

- Providing general information about types of accessibility errors, either as a reference or as feedback to specific errors found with an "accessibility checker" tool.
- Creating wizard-like tools to guide authors in fixing specific errors.

## Authoring tools promote and integrate their accessibility features ([ATAG B.4](https://www.w3.org/TR/ATAG20/#principle_b4))

### Ensure the availability of features that support the production of accessible content ([ATAG B.4.1](https://www.w3.org/TR/ATAG20/#gl_b41))

- To the extent possible, build accessibility features into the natural flow of the authoring process, rather than hiding the accessibility features or making them feel like bolted-on extras that don't really belong.
- Accessibility features should be prominent.
- Don't force users to activate accessibility features. They should be turned on by default.
- If accessibility features can be turned off, warn users when those features are deactivated, and make it easy to re-activate them.

### Ensure that documentation promotes the production of accessible content ([ATAG B.4.2](https://www.w3.org/TR/ATAG20/#gl_b42))

Help features — even those not explicitly about accessibility — should model good accessible techniques. Instructions for adding an image, for example, should show the alt text value even if the article is not about alt text per se. Be vigilant in auditing the examples for anything that inadvertently models bad accessibility techniques.