# Can Websites Detect Screen Readers?

## Web servers can't detect screen readers

Screen readers aren't web browsers, so they don't interact directly with web servers; they interact with the browser, but not with the server. This means that there is no way to tell whether a person is using a screen reader or not, at least not with current technologies.

One thing that a lot of developers often ask is: Can we can write code to detect screen readers? It seems like it would be great to be able to know if a site visitor is using a screen reader, so we can write code just for them, and hide some of the elements that might be harder to make accessible, or less usable with a screen reader, right?

## What if you could detect screen readers?

If you could detect screen readers, would that be a good thing? In theory, you could create an optimized version of the web site for screen reader users, and in theory that could be a good thing, but there are some drawbacks to this idea.

### Separate but (Un)Equal

One of the big concerns about detecting screen readers is that it will result in entirely separate and unequal designs for sighted users versus screen reader users. Screen reader users fear that designers—even when well-intentioned—will create a worse experience for screen reader users. Screen reader users worry that the designers will make too many unwarranted assumptions about what screen reader users want. Designers may strip down the design too far, omitting important aspects of the functionality or content. Or they may change the interface in ways that screen reader users don't expect, reducing usability, even though the intent was to increase usability.

### Maintaining multiple versions is impractical

On a practical level, it's hard to maintain two separate views or designs. The overhead and extra work probably isn't worth it, which means that one of the designs is likely to be neglected. Any guesses as to which design is most likely to be neglected? Yup, the design for screen reader users. The screen reader view will be the "other" view; the invisible view that most users don't even know exists. Soon developers will either forget about it, or they will purposely fail to update it because it's just too much hassle.

### The fear of purposeful neglect based on market percentage

Another fear that blind users have is that web site owners may use usage statistics against people with disabilities. If the web server logs show that only a small percentage of users have screen readers, a web site owner could make a business decision not to support screen readers, based solely on the perceived lack of importance of blind customers. There are two main problems with relying on usage statics to drive that kind of a decision.

If the web site is inaccessible, blind users are unlikely to use it, thus driving down their usage statistics.
Choosing to not support screen reader users is a deliberate choice to discriminate against people with disabilities. Usage statistics are sometimes used to determine things like when not to support a certain browser, or a certain version of a browser. That makes sense, because users can upgrade their browsers as technology marches forward. It's different for screen reader users though. Blind users cannot choose to not be blind. A choice to not support screen readers is a choice to exclude an entire segment of the population, even though yes, it is a minority.

## Additional Resources:

- [Blog article by Steve Faulkner: Developer Beware: Using Flash to Detect Screen Readers](http://www.paciellogroup.com/blog/2008/04/developer-beware-using-flash-to-detect-screen-readers/)
- [Blog article by Marco: Why Screen Reader Detection on the Web is a Bad Thing](http://www.marcozehe.de/2014/02/27/why-screen-reader-detection-on-the-web-is-a-bad-thing/)
