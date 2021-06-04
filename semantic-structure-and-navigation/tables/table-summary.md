# Table Summary

## A summary MAY be provided for data tables.
A table summary is not required. Ideally the table would be simple enough and well-organized enough that the table is self-explanatory just by virtue of the headers and data structure. Even so, it can sometimes be helpful to provide a brief summary of the main points of the table, to help them understand data trends, data format, and/or other aspects of the table that can make the table more understandable to screen reader users.

Summaries should be brief and concise: usually a sentence or two, but perhaps longer for more complex tables. There are a few different ways of presenting table summaries:

- Put the summary in the paragraph preceding or following the table (with aria-describedby)
- Put the summary in the table's `<caption>`, as long as the summary is brief
- Put the table in a `<figure>` and put the title and summary in the `<figcaption>`.
- Put the summary in the summary attribute (for versions of HTML prior to HTML 5)