# Visual Design and Colors: Summary & Checklist

Visual content must be presented so that is it perceivable and understandable by people of differing abilities, including people who are color blind or have low vision, or people who have cognitive, language and learning disabilities.

It must also be presented in ways that accommodate a variety of viewport sizes, from desktop to mobile phone, and browser zoom levels.

## Color

- Any information conveyed by color MUST be accompanied by a programmatically determinable text alternative.
- The text alternative for information conveyed by color MUST accurately convey the same information without color.
- Any information conveyed by color MUST be accompanied by a visible alternative (text, image, etc.) that does not depend on color for meaning.
- Color alone MUST NOT be used to distinguish links from surrounding text unless the color contrast between the link and the surrounding text is at least 3:1 and an additional differentiation (e.g. underline, outline, etc.) is provided when the link is hovered or receives focus.
- Color SHOULD NOT be used as the sole method of distinguishing UI components and/or their surrounding content, unless the color contrast between the UI components and/or surrounding content is at least 3:1.
- Visible text SHOULD be standard text in the markup (not images or graphic versions of text), to allow user customization of text color and contrast.
- Visible UI components SHOULD use native controls and features (not images or graphic versions of controls) where available, to allow user customization of interface color and contrast.

## Contrast

- Small text (under 18 point regular font or 14 point bold font) MUST have a contrast ratio of at least 4.5 to 1 with the background.
- Small text (under 18 point regular font or 14 point bold font) SHOULD have a contrast ratio of at least 7 to 1 with the background.
- Large text and images of large text (at or over 18 point or 14 point bold) MUST have a contrast ratio of at least 3 to 1 with the background.
- Any visual boundary that indicates an active user component's hit area (the region where a pointer can activate the control) MUST have sufficient contrast of at least 3 to 1 with the adjacent background.
- The visual state of an active user interface component MUST have sufficient contrast of at least 3 to 1 with the adjacent background.
- Parts of graphics (required to understand the content) MUST have a contrast ratio of at least 3 to 1 against adjacent color(s).
- The contrast of all visual focus indicators against the background MUST be at least 3 to 1.
- Whenever visual boundaries are used to distinguish controls, the contrast of UI control boundaries compared to adjacent areas MUST be at least 3 to 1 to distinguish the UI control from the adjacent areas.
- Web content MUST retain all essential visual information in Windows High Contrast Mode.
- The design MUST NOT override Windows High Contrast Mode.

## Visual Layout

- Blocks of content SHOULD be visually separated and distinct from each other, via margins, padding, or other methods of achieving visual "white space."
- Labels SHOULD be visually adjacent to their controls.
- The layout SHOULD have only one main visual focus.
- The design SHOULD draw attention to the intended visual focus.

## Target Size

- The touch target size of actionable elements SHOULD be at least 44 pixels by 44 pixels with at least six pixels of inactive space between any adjacent actionable elements.

## Reading Order, Focus Order

- The reading order MUST be logical and intuitive.
- The navigation order of focusable elements MUST be logical and intuitive.
- tabindex of positive values SHOULD NOT be used.

## Typography

- Fonts SHOULD be easily readable by sighted users.
- Line spacing SHOULD be at least 1.5 within paragraphs.
- Paragraph spacing SHOULD be at least 1.5 times larger than the line spacing.
- The number of characters or glyphs per line in any section or column of text SHOULD NOT exceed 80 (40 characters in Chinese, Japanese, or Korean)
- Text SHOULD NOT be full justified.
- Fonts SHOULD be user-customizable.

## CSS-Generated Content and Hidden Content

- CSS-generated content SHOULD be avoided.
- A text alternative for informative CSS-generated content MUST be provided, AND the CSS-generated text SHOULD be set to aria-hidden="true".
- Decorative or redundant CSS-generated content SHOULD be set to aria-hidden="true".
- Visually hidden and inactive content MUST be hidden from screen reader users until that content is made visible and active for sighted users.
- When additional content is triggered on pointer hover or on keyboard focus, that additional content MUST be dismissible, hoverable, and persistent.
