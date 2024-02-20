{
  "date": "2019-10-11",
  "keywords": [
    "XSLFO",
    "XSL Formatting Objects",
    "File",
    "Extension",
    "File Format",
    "Extensible Stylesheet Language"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "Learn about XSLFO file format and APIs that can create and open XSLFO files.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslfo"
    }
  },
  "lastmod": "2021-04-23"
}

## What is an XSL-FO file? ##

XSL-FO (XSL Formatting Objects) is a powerful stylesheet language for formatting XML documents. The semantics of the bounded form of paper and print is expressed by XSL-FO when the dimensions are fixed. In contrast to HTML, which represents the semantics of the unbounded form of a browser window with variable dimensions. The XML documents formatted by XSL-FO are mostly used to generate PDF files. XSL (Extensible Stylesheet Language) is a set of feature-complete W3C technologies intended to design for formatting and exchanging XML documents and XSL-FO part of this language. XSLT and XPath are also other parts of XSL.

It is proposed that XML documents should be transformed first into XSL-FO, PDF is an example of this criteria. In PDF, results are rendered using XSLTfirst, and then XSL-FO formatter. In this fashion, XML documents can be formatted randomly. Though XSL-FO takes the advantage of using Cascading Style Sheet (CSS) properties and extending them where ever necessary for the real format, it houses the provision of page templates called page masters in the terminology of XSL-FO. XSL-FO also provides formatting for fairly sophisticated documents and supports index generation.

## History and Basic Concepts ##

In January 2012 the Working Draft of XSL-FO was updated last time, and in November 2013, its Working Group had been closed. An XSL stylesheet specifies the presentation of a class of XML documents by describing how an instance of the class is transformed into an XML document that uses the formatting vocabulary. XSL-FO is an integrated presentational language and has no semantic markups which are used in HTML. Moreover, this language stores all of the document's data within itself, contrary to CSS which alters the default settings of an external HTML or XML document.

The general criteria of using XSL-FO is that the user writes a document in an XML language rather than writing in FO. After that, an XSLT transform occurs. This XSLT transform is responsible for the conversion of XML into XSL-FO. As soon as, the XSL-FO document is generated, it is then handed over to an application called an FO processor. FO processors are responsible for transforming this document into a readable as well as a printable document. PDF files or PS are examples of the most common output of XSL-FO. But it doesn’t mean that FO processor can only produce these two types of format as output. Some FO processors can output in the RTF files or even a window can appear in the user's GUI, this window displays the page's sequence and their contents.

An XSL-FO document is different from a PDF or a PS in the sense, it does not ultimately define the text layout on different pages. Perhaps, it styles the pages and determines the places to display the contents. Moreover, an FO processor organizes the text within the boundaries specified by the FO document. This specification even permits different FO processors to behave accordingly to the resultant-created pages. An example of such behavior is hyphenation, few FO processors can hyphenate words in order to save space when a line breaks, while some processors don’t select this option. It depends upon the processors to choose different hyphenation algorithms that match their requirements. These hyphenation algorithms may be very simple or maybe more complex. In some situations, XSL-FO specification explicitly sanctions FO processors, some degree of choice in context to the layout.

This variation among FO processors generates varying outcomes, about which processors often remain unconcerned. Because the general focus of XSL-FO is to produced paged/printed documents. XSL-FO documents themselves typically act as intermediaries, their main function is to generate either PDF files or a document that can be printed as the output to be distributed. In HTML/CSS or XSL-FO, distributing the PDF as end result rather than inputting the formatting language indicates that receivers remain unaffected by the resulting versatility which is produced due to differences among interpreters of formatting language. On the other hand, it is evident there is no easy way, that a document can fulfill the different needs of recipients, e.g. variable page size or desired font size, or tailoring for page or print.

## XSLFO File Format ##

SL-FO documents are basically XML documents, but they do not follow any schema. In its place, SL-FO documents follow the syntax defined in the specification of their own language. There are two sections required in each XSL-FO document:

1. A section that specifies a list of labeled page layouts.
1. A section with all the details of document data, with markup, that determines the display of contents on different pages through various page layouts.

Properties of the page are mentioned in the page layouts, which can define the organization for the text, to comply with the conventions for the specific language. Furthermore, the size of the page, their margins, and sequences of pages (that sanctions different properties for the odd and even pages) are also defined by the page layouts.

The data portion of the document is divided into a series of flows, where each flow is connected to a page layout. The flows enclose a list of blocks in them. This list of blocks may contain inline markup features or a list of text data, or maybe both at the same time. Margins of the document may also display the page numbers or chapter headings.  The functionality of both blocks and inline elements remains the same as in the CSS, yet some padding and margin rules are different between FO and CSS.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Multiple columns ##

A page can have multiple columns and blocks and can extend from one column to another by default. Multiple pages are allowed to have different widths and numbers of columns. All FO characteristics follow the limits of a multi-column page.

### Lists ###

An XSL-FO list is established by two sets of blocks arranged cheek by jowl. Conceptually, in a list, a block on the left indicates a number, a bullet, or a string of text, while the right side block may works as anticipated. The numbering of XSL-FO lists is usually done by the XSLT.

### Tables ###

An FO table is similar to an HTML/CSS table. The user can select the rows of data, styling information, background color for each individual cell. Using distinct styling information, the user has the privilege to select the first row as a table header row. The FO processor can be informed explicitly about the space specification of each column, or to auto-fit the text in the table.

### Indexing ###

XSL-FO 1.1 has features that help to generate an index through referencing properly marked-up elements.

### Benefits ###

* Appropriate for content-based publishing
* Ease of use
* Low cost

## References ##

* [What is XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL Formatting Objects](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)
