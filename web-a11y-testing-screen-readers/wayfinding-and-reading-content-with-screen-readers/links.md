# Links

## How screen readers treat links

- Unvisited links: Screen readers typically say "link" then read the link text.
- Visited links: If the user has already been to the link destination, some screen readers will say "visited link", followed by the link text. Others will just say "link".

## Good practices for link text

- <b>Links must have link text.</b> This can be an issue when background images are used as the only content within a link. In those cases, add aria-label="[add your link text here]" to the link element, or use CSS to add visually-hidden text (e.g., using the CSS clip method).
- <b>Make link text descriptive</b> so that the link text makes sense when read out of context (avoid "click here", "here", "more", "read more" or similar).
- <b>Don't say "link" in the link text.</b> Screen readers already say that!
- <b>Use consistent naming of links.</b> If two links on the same page go to the same destination, they should have the same link text. Similarly, links to different destinations should have different link text.

## Navigate through all focusable items

<b>The Tab key:</b> Perhaps the most common way to navigate through the links on the page is to simply use the Tab key (or Shift + Tab to go backward), which causes the focus to land on every focusable element, whether it is a link, a button, a form element, or a custom control of some kind.

If you're interested only in links, this isn't the best method, but it will work, if you don't mind a few extra keystrokes to get past the other focusable items.

## List all links

- JAWS with Chrome, Edge, Firefox, IE: Insert + F7
- NVDA with Firefox, Chrome, Edge: Insert + F7 (to show Elements List), then choose links
- VoiceOver with Safari (iOS): Not available
- Talkback with Chrome, Firefox: Not available
- VoiceOver with Safari (macOS): Control + Option + U (to open the Rotor), then use left or right arrows to select links
- Narrator with Edge: Caps Lock + F7

## Navigate from one link to the next

- JAWS with Chrome, Edge, Firefox, IE: Not available
- NVDA with Firefox, Chrome, Edge: K
- VoiceOver with Safari (iOS): Use the rotor to select links (twist to fingers on the screen to left or right), then swipe down with one finger
- Talkback with Chrome, Firefox: Local context menu (swipe up then right), then select links
- VoiceOver with Safari (macOS): Control + Option + Command + L
- Narrator with Edge: K (in Scan Mode only)

## Navigate unvisited links only

- JAWS with Chrome, Edge, Firefox, IE: U
- NVDA with Firefox, Chrome, Edge: U
- VoiceOver with Safari (iOS): Not available
- Talkback with Chrome, Firefox: Not available
- VoiceOver with Safari (macOS): Not available
- Narrator with Edge: Not available

## Navigate visited links only

- JAWS with Chrome, Edge, Firefox, IE: V
- NVDA with Firefox, Chrome, Edge: V
- VoiceOver with Safari (iOS): Not available
- Talkback with Chrome, Firefox: Not available
- VoiceOver with Safari (macOS): Control + Option + Command + V
- Narrator with Edge: Not available
