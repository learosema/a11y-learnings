# Testing for Sufficient Color Contrast

## Test for Sufficient Color Contrast Between Text and Background

Ensuring that color contrast is at least 4.5:1 for small text or 3:1 for large text can be difficult to discern just by looking at the colors. Even though some low contrast combinations may sometimes be obvious (dark red against black, for instance), it is critical that you utilize tools to determine if the colors you use meet the minimum contrast ratio requirements.

The research and empirical findings used to calculate the contrast ratios and establish the minimum contrast requirements take into consideration the loss in contrast people with moderate low vision or colorblindness may have.

## Testing Color Contrast Using axe

The Accessibility Engine, axe, is the third generation of accessibility rules for HTML-based user interfaces. It is a publicly available testing tool that returns zero false positives and works in all modern web browsers. Because it is an open source JavaScript library, it is highly configurable and can be integrated into existing functional accessibility testing.

One of the accessibility rules built into axe is a rule for color contrast. The color contrast rule in axe analyzes contrast and ensures that contrast between foreground and background colors meet WCAG 2.1 AA contrast ratio thresholds. So, when an analysis is conducted through axe, color contrast is automatically evaluated.

## Color Contrast Analysis Tools

The contrast ratios may not mean much to you at this point. Don't worry about that. You don't have to memorize color combinations or contrast ratios. There are plenty of tools available to help you analyze the contrast ratio of your colors and tell you if they pass the guidelines or not. Here are a few of them:

- [axe](http://www.deque.com/products/axe/) — the Accessibility Engine is an open-source JavaScript accessibility rules library that is fast, returns no false positive errors or duplicate results, and is publicly available as a GitHub repository, browser plugin, or framework integration
- [Deque color contrast analyzer](https://dequeuniversity.com/color-contrast)
