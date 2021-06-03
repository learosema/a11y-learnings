# WCAG guidelines benefitting cognitive disabilities

## Overview

Even though WCAG 2.1 does not fully address the needs of people with cognitive disabilities, it does have a few relevant guidelines worth mentioning.

One of the other issues is that some of these guidelines are not specific to people with cognitive disabilities. They are general enough that they apply to pretty much all audiences. That's a good thing in the sense that it proves that there are collateral benefits for everyone when designing with accessibility in mind. It's a bad thing, though, in the sense that it makes it somewhat hard to make the case that there is a clear link between these guidelines and cognitive disability accessibility specifically.

The WCAG guideline with the clearest link to cognitive disabilities is 3.1.5: Reading Level.

### Note:
Some users with reading disabilities (and some other kinds of cognitive disabilities) use screen readers to supplement their reading abilities, so all of the WCAG guidelines that address screen reader accessibility also apply to these users. Most people with cognitive disabilities do not use screen readers, though, so screen-reader-specific guidelines are not included in the list on this page.

## WCAG single-A guidelines

### 2.5.2 Pointer Cancellation: 

For functionality that can be operated using a single pointer, at least one of the following is true (Level A):

- No Down-Event: The down-event of the pointer is not used to execute any part of the function;
- Abort or Undo: Completion of the function is on the up-event, and a mechanism is available to abort the function before completion or to undo the function after completion;
- Up Reversal: The up-event reverses any outcome of the preceding down-event;
- Essential: Completing the function on the down-event is essential.

How this pertains to cognitive disabilities: All users benefit from an abort or undo feature that makes fixing mistakes easier. Users with cognitive disabilities might especially benefit from this feature.

#### Techniques for 2.5.2

Techniques to accomplish this include:

- Ensure that drag-and-drop actions can be cancelled.
- Ensure that touch events are only triggered when touch is removed from a control.

### 3.3.1 Error Identification

If an input error is automatically detected, the item that is in error is identified and the error is described to the user in text. (Level A)

How this pertains to cognitive disabilities: Everybody needs to know when an error occurs, what the error is, and how to fix it. People with cognitive disabilities, especially, may have a hard time figuring out what the problem is if they don't receive guidance.

#### Techniques for 3.3.1

Techniques to accomplish this include:

- When an error occurs, post an error message adjacent to the element with an error (e.g. the form field) with a clear, succinct error message that explains what the error is (e.g. "The email address you typed is not valid."

### 3.3.2 Labels or Instructions

Labels or instructions are provided when content requires user input. (Level A)

How this pertains to cognitive disabilities: Labels and instructions are good for everyone but can be particularly important for people with cognitive disabilities. The instructions for users with cognitive disabilities may have to be more explicit, clearer, and written in simpler language. It may even be best to put the instructions in a video or audio format.

#### Techniques for 3.3.2

Techniques to accomplish this include:

- Ensure every interactive element has a clearly-written, accurate label visually adjacent to the element.
- Provide instructions whenever there is a possibility of confusion.
- Ensure the instructions are written clearly and succinctly.

## WCAG double-A guidelines

### 1.3.5 Identify Input Purpose

The purpose of each input field collecting information about the user can be programmatically determined when: (Level AA)

- The input field serves a purpose identified in the Input Purposes for User Interface Components section; and
- The content is implemented using technologies with support for identifying the expected meaning for form input data.

How this pertains to cognitive disabilities: Users with cognitive disabilities might have difficulty with filling out forms. They may also prefer to use custom icon sets to label forms rather than words. Having a form that can be automatically filled out can be very helpful.

#### Techniques for 1.3.5

Techniques to accomplish this include:

- Use HTML 5.2 autocomplete attributes.

### 1.4.12 Text Spacing

In content implemented using markup languages that support the following text style properties, no loss of content or functionality occurs by setting all of the following and by changing no other style property: (Level AA)

- Line height (line spacing) to at least 1.5 times the font size;
- Spacing following paragraphs to at least 2 times the font size;
- Letter spacing (tracking) to at least 0.12 times the font size;
- Word spacing to at least 0.16 times the font size.

How this pertains to cognitive disabilities: Users with dyslexia might find it easier to read with extra spacing, and they may also use custom fonts to enhance readability.

#### Techniques for 1.4.12

Techniques to accomplish this include:

- Allow for text spacing override in CSS.
- Allow for text spacing without wrapping in CSS.

### 1.4.13 Content on Hover or Focus

Where receiving and then removing pointer hover or keyboard focus triggers additional content to become visible and then hidden, the following are true: (Level AA)

- Dismissible: A mechanism is available to dismiss the additional content without moving pointer hover or keyboard focus, unless the additional content communicates an input error or does not obscure or replace other content;
- Hoverable: If pointer hover can trigger the additional content, then the pointer can be moved over the additional content without the additional content disappearing;
- Persistent: The additional content remains visible until the hover or focus trigger is removed, the user dismisses it, or its information is no longer valid

How this pertains to cognitive disabilities: All users need time to perceive, read, and process new content. Users with cognitive disabilities might find it particularly frustrating if content appears briefly and then disappears before they have a chance to review it.

#### Techniques for 1.4.13

Techniques to accomplish this include:

- For ARIA: Use role="tooltip".
- For CSS: Use hover and focus pseudo classes.

### 3.2.3 Consistent Navigation

Navigational mechanisms that are repeated on multiple Web pages within a set of Web pages occur in the same relative order each time they are repeated, unless a change is initiated by the user. (Level AA)

How this pertains to cognitive disabilities: It can be disorienting when the interface—especially the main navigation—changes between views or pages. Some people with cognitive disabilities have a low tolerance for change and will find it difficult to learn new interfaces.

#### Techniques for 3.2.3

Techniques to accomplish this include:

- Use a template that places the navigation in the same location across all pages.
- Keep the relative order of the links in the navigation the same.
- Do not remove the current page from the navigation. It may be a good idea to make the reference to the current page non-linked text, rather than a link, depending on the context, but leave a reference to the current page in the navigation list.


### 3.2.4 Consistent Identification

Components that have the same functionality within a set of Web pages are identified consistently. (Level AA)

How this pertains to cognitive disabilities: Some people with cognitive disabilities will not be able to recognize that two names may refer to the same thing.

For example, if there are two links, "Contact us" and "Call us," that point to the same web page, it is not immediately apparent that they would or should point to the same page. 

Another example: If there is a 5-step process, with each step requiring the user to click on a link to the go the next page, the word in the link should be consistent. It could say "Next" or "Continue" or some other word could be used, but it should always be the same word. Don't mix and match words.

#### Techniques for 3.2.4

Techniques to accomplish this include:

- Use the same text for all links that refer to a particular web page or destination.
- Use the same text for all buttons that perform a similar function.
- Use the same text when referring to the same content elements (e.g. a table, a form, an image, etc.)

### 3.3.3 Error Suggestion

If an input error is automatically detected and suggestions for correction are known, then the suggestions are provided to the user, unless it would jeopardize the security or purpose of the content. (Level AA)

How this pertains to cognitive disabilities: Some people with cognitive disabilities can become confused, disoriented, or discouraged if there is an error but they don't know why or how to fix it.

#### Techniques for 3.3.3

Techniques to accomplish this include:

- In addition to, or instead of, an error identification message (see 3.3.1: Error Identification), post a message explaining how to fix the error.
- Example 1 (error identification, followed by an error correction suggestion): "Error: Email is not valid. Your email address must include the @ symbol."
- Example 2 (error identification and an error correction suggestion rolled into one):
"Error: You must choose a size."

### 3.3.4 Error Prevention (Legal, Financial, Data)

For Web pages that cause legal commitments or financial transactions for the user to occur, that modify or delete user-controllable data in data storage systems, or that submit user test responses, at least one of the following is true: (Level AA) 

1. Reversible: Submissions are reversible.
2. Checked: Data entered by the user is checked for input errors and the user is provided an opportunity to correct them.
3. Confirmed: A mechanism is available for reviewing, confirming, and correcting information before finalizing the submission.

How this pertains to cognitive disabilities: People with cognitive disabilities are among the most likely to make mistakes. It is best to help them avoid mistakes before they become permanent.

#### Techniques for 3.3.4

Techniques to accomplish this include:

- Summarize for the user all of the data to be submitted before the user officially submits it.
- Ask the user to confirm the submission (e.g. "Are you sure you want to delete this file?")
- Play a brief warning sound, accompanied by a visual warning, when the user submits the data, then confirm the user's intentions.
- Allow a grace period after submission of data in which the submission can be altered or cancelled.
- Where appropriate, provide a "recycle bin" that captures deleted data where it can be recovered later.

## WCAG triple-A guidelines

### 1.3.6 Identify Purpose

In content implemented using markup languages, the purpose of User Interface Components, icons, and regions can be programmatically determined. (Level AAA)

How this pertains to cognitive disabilities: This success criterion is designed to help users customize their web experience. Users who find it easier to understand sets of icons than words would be able to place custom sets of icons on the screen through assistive technology. They could also hide extraneous regions of the page to help them focus on the content they want to see. This would be helpful to users who experience difficulty with reading, processing, or maintaining focus.

#### Techniques for 1.3.6

Techniques to accomplish this include:

- Use ARIA landmarks to identify regions of a page.
- Future technique (not yet available): use HTML microdata to markup user interface components.

### 2.2.6 Timeouts

Users are warned of the duration of any user inactivity that could cause data loss, unless the data is preserved for more than 20 hours when the user does not take any actions. (Level AAA)

How this pertains to cognitive disabilities: Users with cognitive disabilities might take extra time to complete tasks. Ensuring that users are warned before a timeout can allow them to save their work or extend their session, so they don’t have to start from scratch.

#### Techniques for 2.2.6

Techniques to accomplish this include:

- Set a session timeout to occur following at least 20 hours of inactivity.
- Store user data for more than 20 hours.
- Provide a warning of the duration of user inactivity at the start of a process.

### 3.1.3 Unusual Words

A mechanism is available for identifying specific definitions of words or phrases used in an unusual or restricted way, including idioms and jargon. (Level AAA)

How this pertains to cognitive disabilities: Reading abilities vary. Some people cannot read at all. Others can read only at lower education levels.

#### Techniques for 3.1.3

Techniques to accomplish this include:

##### In written text:

- Define the word(s) inline, in the context of the text itself, immediately after the word appears in the text.
- Example 1: "A parsimonious society (a society that is frugal to the point of being stingy) risks exacerbating relationships (making the relationships worse) between the rich and poor."
- Example 2: "A parsimonious society risks exacerbating relationships between the rich and poor (parsimonious = frugal to the point of being stingy; exacerbating = making worse)."
- Define the word(s) in a tooltip (ARIA role="tooltip") that is activated by mouse hover and keyboard focus. If the word(s) appear frequently, the source of the tooltip definitions could be a centralized database or file used throughout the website.
- Example: "A parsimonious person cannot be expected to pay a generous tip."
- Create a definition list (<dl>) defining unusual words. The definition list might be at the bottom of the page, or on a separate page in a glossary of terms. Be sure to create a link from the unusual word to the definition. Otherwise, the definition will be too hard to find.
- Provide a function that allows users to find definitions in an online dictionary.

##### In multimedia:

- Write the script so that any unusual words are explained by the narrator, in the dialog, or in an additional audio track created explicitly for accessibility purposes. If a separate audio track is used, the video could be presented in two versions: one without the additional explanations, and one with the additional explanations. Ensure that the version with additional explanations is easy to find and that its purpose is clearly labeled.
- Show the definition of the word(s) on the screen, preferably with accompanying narration so that all audiences — even those who cannot read or who cannot see — get the benefit of having the definition.
- For people with cognitive disabilities, the first option (defining the words inline) is probably the best, because when the word is defined immediately in the context, the user doesn't have to figure out how to find the definition and doesn't have to figure out how to get back to the original location. The tooltip option is a good second choice because the user doesn't have to leave the current location.

### 3.1.4 Abbreviations

A mechanism for identifying the expanded form or meaning of abbreviations is available. (Level AAA)

How this pertains to cognitive disabilities: Some people with cognitive disabilities do not know the meaning of some acronyms (indeed, this is true of many people without cognitive disabilities too). Also, the concept of what an acronym is may be difficult for some people with cognitive disabilities to understand.

#### Techniques for 3.1.4

Techniques to accomplish this include:

##### In written text:

- Expand the abbreviation inline, in a parenthetical clause, or some other similar way.
- Example: "The divers used SCUBA (Self-Contained Underwater Breathing Apparatus) gear to explore the underwater portions of the cave."
- Make the abbreviation available in a tooltip (ARIA role="tooltip") that is activated by mouse hover and keyboard focus.
- Example: "The divers used SCUBA gear to explore the underwater portions of the cave."
- Encode the expansion of the abbreviation in the <abbr> element, making it available on mouse hover in most browsers, and available to most screen readers. The expansion is still unavailable to keyboard users, unfortunately. Example:
Example code: <abbr title="Self-Contained Underwater Breathing Apparatus">SCUBA</abbr>
Example result: SCUBA

##### In multimedia:

- Write the script so that abbreviations are explained by the narrator, in the dialog, or in an additional audio track (optionally in a separate version of the video).
- Show the acronym and its expansion on the screen, preferably with accompanying narration for the benefit of those who cannot read or who cannot see.


### 3.1.5 Reading Level

When text requires reading ability more advanced than the lower secondary education level after removal of proper names and titles, supplemental content, or a version that does not require reading ability more advanced than the lower secondary education level, is available. (Level AAA)

How this pertains to cognitive disabilities: The comprehension levels of people with cognitive disabilities varies widely, from highly sophisticated at one end of the spectrum to very little language comprehension at the other. 

For those who experience difficulty processing language or reading, it can help to use simple words and simple sentence construction.

#### Techniques for 3.1.5

Techniques to accomplish this include:

##### In written text:

- Write at the lowest reading level possible that is still appropriate for the content.
- Provide a summary, in simple language, at the top of the content, or available from a link (to another page, or another part of the same page) or button (to a dialog or similar) at the top of the content.
- Write a second version of the content in simpler language than the original version, and make both versions available to users.
- Supplement the text with illustrations, audio, video, or other formats.

##### In multimedia:

- Write the script at the lowest reading level possible that is still appropriate for the content.
- Provide an audio or audiovisual summary of the content in simple language.
- Create a second version of the multimedia content that uses simple language. Make both versions available to users.
- Take advantage of the audiovisual aspects of multimedia to create animations, demonstrations, or other non-verbal methods of illustrating concepts.

##### Determining reading level:

WCAG recommends a "lower secondary education level" for the reading level. How can you know if you've achieved that level? One way is to run an automated readability test (ReadabilityFormulas.com). While imperfect, they do give a general sense of the reading level. It's best to test using more than one method. The test in the previous link shows the scores of 7 different readability algorithms and provides a composite score.

### 3.1.6 Pronunciation

A mechanism is available for identifying specific pronunciation of words where meaning of the words, in context, is ambiguous without knowing the pronunciation. (Level AAA)

How this pertains to cognitive disabilities: Sometimes a person will know a word when they hear it but will not know it in its written form. Having a pronunciation guide can help.

#### Techniques for 3.1.6

Techniques to accomplish this include:

##### In written text:

- Write out the pronunciation inline, in the context where the word occurs.
- Include a tooltip (available with either mouse hover or keyboard focus) with the pronunciation written out.
- Include the pronunciation in a glossary at the bottom of the page, or on a separate page. Provide a link to the glossary from the words in the text.
- Provide an audio file with a recording of someone saying the word(s).

##### In multimedia:

- Any time the words appear on the screen, ensure the narration or dialog speaks the words out loud.
- Should you use official linguistic syntax?
- Linguists have a precise way of writing the pronunciation for sounds, using internationally-recognized linguistic glyphs. Unfortunately, most people don't know how to interpret all of those glyphs, so it may help to write the pronunciation phonetically instead.

For example, Merriam Webster writes the pronunciation for the word "pronunciation" as follows:

\prə-ˌnən(t)-sē-ˈā-shən also ÷-ˌnau̇n(t)-\

Some people know what that means, and that is the correct way to write it when linguistic precision matters, but in other cases it may be helpful to write it more like this:

pro-nun-see-AY-shun

That's easier for most people to understand.

### 3.2.5 Change on Request

Changes of context are initiated only by user request or a mechanism is available to turn off such changes. (Level AAA)

How this pertains to cognitive disabilities: Some people with cognitive disabilities become confused when the interface changes, especially when the users themselves don't request the changes.

#### Techniques for 3.2.5

Techniques to accomplish this include:

- Ensure that no significant events (e.g. loading new pages or changing the interface) happen as a result of events like hover, focus, or form element changes. Instead, use events like the activation of a link or button.

### 3.3.5 Help

Context-sensitive help is available. (Level AAA)

How this pertains to cognitive disabilities: People with cognitive disabilities are among the most likely to need help.

#### Techniques for 3.3.5

Techniques to accomplish this include:

- Provide a help link on each page, with help documentation specific to that page.
- Provide a link to a live chat feature, to contact someone who can assist.
- Provide brief inline help text (e.g. formatting hint, explanation of what the item means, etc.), visible at all times, adjacent to the relevant element (form field, widget, etc.)
- Provide pop-up help (e.g. a button with a question mark icon  or an "I" icon  that opens a tooltip or dialog) next to form fields or widgets that might need extra explanations).
- Provide a link to a phone number, to call someone who can assist.

### 3.3.6 Error Prevention (All)

For Web pages that require the user to submit information, at least one of the following is true: (Level AAA)

1. Reversible: Submissions are reversible.
2. Checked: Data entered by the user is checked for input errors and the user is provided an opportunity to correct them. 
3. Confirmed: A mechanism is available for reviewing, confirming, and correcting information before finalizing the submission.

#### Note:

This guideline is essentially identical to 3.3.4 Error Prevention (Legal, Financial, Data), except that the scope is not limited to legal, financial, and data situations.
