# Documents (Word, PDF, EPUB)

## An HTML version of non-HTML content SHOULD be made available to users.

The first general guideline with regard to non-HTML content is to avoid posting the information only in a non-HTML format, if possible. Standard HTML is one of the most accessible formats available, and is the most appropriate format for web content, for the following reasons:

- The accessibility features in HTML are quite mature, in most cases exceeding the accessibility features of non-HTML platforms.
- Users don't need to download the file.
- Users don't need to leave the web browser interface.
- Users don't need to own, download, or install extra software.

Posting a non-HTML document can be appropriate when it is necessary to retain printer styling (e.g., with the PDF format), or when it is necessary to share files in their original format for collaboration purposes (e.g., with MS Office documents).

Even so, it is usually best to provide either provide the full content in HTML format also, or, at a minimum, provide a summary of the content in HTML format.

## Non-HTML documents MUST adhere to basic accessibility principles.

Here are some of the most basic principles for document accessibility across many kinds of formats:

- Give the document a meaningful title
- Provide good heading structure
- Provide alternative text for images
- Designate table headers and ensure the data cells are associated with the headers
- Don't rely on color alone to convey information
- Ensure sufficient contrast between the text and the background
- Choose highly readable fonts


## PDF files MUST be in tagged PDF format.

The PDF format includes an accessibility API that is very similar to HTML. Content is wrapped in tags that designate semantic elements and structure. A PDF file must be in "tagged PDF" format to be accessible to screen readers. Untagged PDF files cannot be read at all by screen readers. 

Adobe Reader and Acrobat Pro have a feature to auto-tag documents when the file is accessed using a screen reader, but the auto-tagging process is imperfect. It makes its best guesses as to what the tags should be, and often guesses incorrectly, especially when the document was not created with accessibility in mind to begin with. 

The resulting auto-tagged file may be acceptable in the case of simple content but can be woefully inadequate with more complex content.

To create a tagged PDF file, start by creating an accessible document in the original authoring software, such as Word or InDesign. 

Export the document to PDF format, and then use Acrobat Pro to check to make sure the tagged document accurately represents the accessibility intent of the original document. In most cases, the document will require some touch-up in Acrobat Pro.

The W3C maintains a list of [PDF accessibility techniques](https://www.w3.org/WAI/WCAG21/Techniques/#pdf) with respect to WCAG 2.1 conformance.

### Note 

It is possible to do all of the accessibility tagging of an inaccessible document in Acrobat Pro, but most of the work of making a PDF document accessible is usually easiest to accomplish within the original authoring tool (e.g., Word, InDesign, etc.).

## EPUB files MUST adhere to HTML accessibility principles, and the accessibility principles of any other technologies used within the EPUB document.

EPUB is an electronic book (eBook) format based on the structure of HTML, so virtually all web accessibility principles apply to EPUB documents.

There are several competing technologies for eBooks. EPUB is arguably the most accessible of them all, because EPUB documents are essentially HTML documents gathered together in a convenient book-like format. An EPUB reader is required to view EPUB documents. You can include images, multimedia, MathML, and other technologies within the EPUB document, in almost the same way that you would include them in HTML documents.

EPUB documents are flexible in the way they present content. EPUBs are built in such a way that an EPUB reader can allow users to magnify the text, change colors, increase contrast, and manipulate the styles, though the degree to which this is possible varies from one EPUB reader to the next. Accessibility and user control are among the strengths of the EPUB format.

By way of contrast, PDF documents are much less flexible and user configurable because PDF documents are designed to retain their visual styling and layout. PDF documents are appropriate for printing purposes or when strict visual layout is a requirement. EPUB documents are more appropriate in most other circumstances.

## EPUB files SHOULD be in EPUB 3 format.
The EPUB 3 format includes a substantial number of accessibility improvements over prior versions, so you will obtain the best results with the most current version. Presumably future versions of EPUB will also have good accessibility support, possibly with additional enhancements.

## EPUB documents MUST adhere to the additional accessibility principles in the EPUB Accessibility specification.
Just as PDF files must be built according to its respective accessibility API, EPUB files must take into account the EPUB accessibility specification.

EPUB accessibility resources:

- [General EPUB 3 accessibility information](https://idpf.github.io/a11y-guidelines/)
- [EPUB Accessibility 1.0 (proposed specification)](http://www.idpf.org/epub/a11y/)
