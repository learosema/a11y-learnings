# Link Text

# A link MUST have programmatically determinable text, as determined by the accessible name calculation algorithm.

A link must have a text-based name associated with it so that screen readers can read something to users. If a link has no name associated with it, most screen readers will read the link destination in the href as a way to give users some sort of clue to the purpose of the link.

The name of a link is calculated as follows (in order of precedence by screen readers):

1. aria-labelledby
2. aria-label
3. Text contained between the opening <a> and closing </a> elements (including alt text on images)
4. title attribute (last resort)

Even though the native text of the link is third on the list in the name calculation, it should be the first thing that you consider when creating link text. Other methods are for more complex situations.

# The purpose of each link SHOULD be able to be determined from the link text alone.

Screen reader users often listen to links out of context, either by navigating through the links, or by using a keyboard command to list all of the links on the page. The best technique is to make sure all links make sense out of context.

| Bad Link Text   | Good Link Text                                     |
|-----------------|----------------------------------------------------|
| Click here      | Computer configuration options                     |
| Here	          | an article about bees on the Smithsonian web site  |
| Read more       | Read more about gaming memes                       |
| More	          | More about the scientific method                   |

# The link text SHOULD NOT repeat the role ("link").

Screen readers will say "link" and then read the link text, so there is no need to include the word "link" in the link text.

# Features such as labels, names, and text alternatives for content that have the same functionality across multiple web pages MUST be consistently identified.

## Bad examples

```html
<p><a href="contact.html">Our Company</a></p>
<p><a href="contact.html">Contact Us</a></p>

<!-- or -->
<p><a href="contact.html"></a>Contact Us</a></p>
<p><a href="directory.html">Contact Us</a></p>
```
