{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PDF/UA File Format",
  "description":"Learn about PDF/UA file format and APIs that can create and open PDF/UA files.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is PDF/UA file? #

PDF/UA was published as [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) in August 2012 and is by far the first complete definition of a set of requirements for universally accessible PDF documents. The term "universally accessible" refers to the understanding that the information contained in a [PDF](/pdf/) document should be equally and independently accessible to everyone in general and to people with disabilities in particular. Introduction of the PDF/UA standard can be considered a major step for creating tools and applications in order to create and read PDF content.

## File Format Requirements ##

The PDF/UA has some definite requirements at its base that act as the essence of this standard. Essentially, these are based on tagging PDFs which means that all PDF/UA documents must be properly tagged. It also requires the tags to be semantically appropriate and in logical order. This ensures that the end document created with PDF/UA spec is more reliable and accessible. This may bring PDF authors to question if they need to know everything about all such requirements? Luckily, it's not like this as the PDF/UA conformance tools take the responsibility for adding and preserving the accessibility of the PDF.

The file format requirements for PDF/UA are as follow.

* Content is categorised in one of two ways: meaningful content, and artefacts such as decorative page elements. All meaningful content must be tagged and integrated into the structure tree of all tags within a document. Artefacts, on the other hand, need only be marked as such.
* Meaningful content must be marked with tags and, together with the other tags in the document, create a complete structure tree.
* Meaningful content must be marked with the appropriate semantic tags.
* The structure tree created by the document tags must reflect the document’s logical reading order.
* Only the standard tags defined in PDF 1.7 may be used; if any other tags are used, a role assignment entry must record which standard tag each one represents.
* Information may not be conveyed using visual means alone (e.g. contrast, colour or position on the page).
* No flickering, blinking or flashing content is permitted, either as effects controlled by JavaScript or as part of any videos embedded within the PDF.
* A document title must be given, and the document must be set up so that the title (rather than the file name) appears in the window title.
* The language of all content must be noted, and changes of language must be explicitly marked as such.

## PDF/UA Conformance ##

The PDF/UA standard defines specifications for content, readers and assistive technology. These three aspects are linked with each other based on the contents of the document. The conformance requirements for each of these are as mentioned below.

## Conforming Files ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Conforming Readers ##

A conforming reader must obey the rules spelled by PDF 1.7 specifications. Specifically, it should support:

* all the tags, attributes and key values specified for accessibility. It should also have the ability to process and represent digital signatures, annotations and Optional Content.
* process and represent digital signatures, annotations and Optional Content
* navigate the document by a variety of means

## Conforming Assistive Technology ##

A conforming assistive technology is bound for supporting the PDF/UA features. These include, for example, features of the content and the reader, and should allow navigation by page labels, document structure, or the outline. It should also let the user override default navigation zoom.

## References ##

* [PDF/UA - By Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA in a Nutshell](https://pdfa.org/pdfua-in-a-nutshell/)
