# Complete Start and End Tags

# In content implemented using markup languages, elements MUST have complete start and end tags.
Note also that start and end tags that are missing a critical character in their formation, such as a closing angle bracket or a mismatched attribute value quotation mark, are not complete.

You can use various validator tools such as [The W3C Markup Validation Service](http://validator.w3.org/) to validate your markup.

Almost all modern browsers repair the source code (when incomplete start or end tags, improper nesting and duplicate attributes are found). So, if you look at the DOM version of the page, remember you are not looking at the true source. Because the purpose of this checkpoint is to ensure the web content meets specific HTML grammar requirements, the actual source code is what needs to be checked (not the DOM).

