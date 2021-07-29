# Abbreviations and Acronyms

## How screen readers treat abbreviations

- <b>Pronounceable abbreviations</b>: Screen readers generally try to pronounce acronyms and nonsensical words if they have sufficient vowels and consonants to be pronounceable; otherwise, they spell out the letters. For example, NASA is generally pronounced as a word, whereas DHS is pronounced as individual letters: "D H S."
- <b>Unpronounceable abbreviations</b>: If screen reader users don't understand a word read by the screen reader, they can have the screen reader read it letter by letter. When reading words letter by letter, the screen reader distinguishes between uppercase and lowercase letters by emphasizing the uppercase letters in a higher pitch or louder voice.

## Expand the first instance of an abbreviation

It's best to expand the first instance of an abbreviation on a web page, so that there is no confusion as to what the abbreviation means.

## Semantic markup for abbreviations

You can use the `<abbr>` element to mark abbreviations and acronyms.

### Good example: An abbreviation marked with `<abbr>`

```html
<abbr title="Self-Contained Underwater Breathing Apparatus">SCUBA</abbr>
```

Some screen readers read full expanded text of the abbreviation when you do this. Others read only the visible text. In most cases screen readers allow users to customize the behavior when reading abbreviations.
