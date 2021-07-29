# No Visual Styles

## Screen readers ignore almost all CSS styles

Although there are ways to expose some aspects of the styling by customizing screen reader settings, screen reader users will generally NOT be aware of any of the following:

- Color
- Background color
- Background images
- Font size
- Font style
- Bold
- Italic
- All capitals (unless the user listens to the word character by character)
- Visual position
- Visual spacing between items
- Columns or floating containers

If you are using CSS to convey meaning—such as using a background color to highlight text—be sure to supplement the CSS with actual text that conveys the same meaning. For example, you could prefix the highlighted text with the word "Important:".

## Screen readers hide content marked as `display:none`

One CSS property that screen readers do pay attention to is `display:none`. Screen readers ignore everything marked as `display:none`, and do not let users access it. You can use this to your advantage when hiding things like submenus, inactive dialogs, etc. You don't want screen reader users to access those elements in their hidden or inactive state. Marking them with display:none is appropriate in those cases.
