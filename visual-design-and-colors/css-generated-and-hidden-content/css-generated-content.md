# CSS-Generated content

## CSS-generated content SHOULD be avoided.

CSS-generated content is supported by NVDA + Firefox, NVDA + Chrome, VoiceOver on OS X + Safari, and VoiceOver on iOS + Safari. It is not supported by JAWS + Internet Explorer or by Narrator + Edge. Given the lack of universal support, it is best to avoid CSS-generated content, especially if that content is meaningful and not just for decoration.

(TODO: test again in Narrator if this information is still up2date)

### Good example

It can be appropriate to use CSS-generated content for printing purposes (which is essentially irrelevant to screen reader users). In the example below, the href value is taken from the <a> element and shown after the original link text, with the goal in mind of ensuring that people who read a web page printed on paper can type in the link if they want to.

```html
a.generated::after {
    content: " ( " attr(href)  ") ";
}
```

## A text alternative for informative CSS-generated content MUST be provided, AND the CSS-generated text SHOULD be set to aria-hidden="true".

Even though CSS-generated content should be avoided under most circumstances, there may be some acceptable uses of it. 

If the generated content is informative — in other words if a blind user needs to know about the content — then a text alternative must be provided to account for the screen reader limitations of JAWS + Internet Explorer and Narrator + Edge. 

If both of those browsers supported CSS-generated content, there would be no need to provide a text alternative.

It gets a little complicated because some screen readers do support CSS-generated content. To take all scenarios into account, developers should hide the generated text from all screen readers using aria-hidden="true" and provide a text alternative some other way, such as via aria-label, if the item is a link, button, form control, or other focusable item.

If it is not a focusable item, it may be necessary to use a technique such as CSS hidden text (using position:absolute; clip:rect(0 0 0 0)).

## Decorative or redundant CSS-generated content SHOULD be set to aria-hidden="true".

If the CSS-generated content is purely for visual decoration, or if it is redundant with the adjacent text, it's usually appropriate to set the CSS-generated content to aria-hidden="true", to ensure that screen readers don't read the unnecessary text.