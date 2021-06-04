# `<strong>` and `<em>`

## Critical emphasis in the text SHOULD be conveyed through visual styling.

Sometimes you want to emphasize text. Visually you can create emphasis with bold or italics. In HTML there are even semantic elements created with this exact purpose in mind: `<em>` for emphasis (italics) and `<strong>` for strong emphasis (bold).

## Critical emphasis in the text SHOULD be conveyed in a text-based format.

Sadly, all major screen readers ignore both the `<em>` and the `<strong>` elements, at least in their default configuration. Some (but not all) screen readers allow users to change the settings so that the `<em>` and the `<strong>` elements are acknowledged by the screen reader. If users have the right screen reader, and if they are savvy enough to know that the setting exists, and if they change the setting, they will benefit from `<em>` and `<strong>`, but you can't count on that for the vast majority of users.

If you need to emphasize text — if the emphasis is critical to understand the text — then you'll need to find another way to create emphasis.

## Note

If the emphasis is not critical to understanding the meaning, it is not necessary to ensure that the emphasis is accessible to screen readers. If the content is understandable without the emphasis, you can consider it optional to find a way to make the emphasis accessible. Screen reader users are used to not hearing things emphasized. It's true that they will sometimes miss the nuances this way, but if the main message is still accessible, that may be acceptable, even if it's not ideal.

For the times when it is necessary to make the emphasis accessible, there are a few different options.

## Example 1: Visible text

This is the most straightforward technique. You can add words like "Important" or "Warning" to your text to make sure that the content is emphasized.

```html
<p>Important: You cannot undo. Your file will be permanently deleted.</p>
```

## Example 2: Add invisible text

```html
<p><span class="visually-hidden">Important:</span>
You cannot undo. Your file will be permanently deleted.</p>
```

## Example 3: Prepend a warning image

```html
<p><img src="warning.png" alt="Warning"> 
You cannot undo. Your file will be permanently deleted.</p>
```
