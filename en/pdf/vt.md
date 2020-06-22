{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PDF/VT",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is PDF/VT? #

PDF/VT, published as [ISO 16612-2](https://www.iso.org/standard/46428.html) in August 2010 as a standard, is designed to enable variable document printing (VDP) in a variety of environments. The standard makes Variable information and Transactional printing as its basis for the standard. The Variable data printing is used where part of information is different for each recipient of the content. The Transactional printing includes invoices, statements and other documents that combine billing information with marketing information. This results in a mix of improved processing of images, text and other content types. PDF/VT enables reliable and dynamic management of pages for High Volume Transactional Output (HVTO) print data by using the document part metadata (DPM) concept. PDF/VT files can be opened in Adobe Acrobat viewer without the need of adding any other component.

## Document Part Hierarchy ##

The Document Part  (DPart) Hierarchy is like a tree-structure of document part nodes that is based on all pages in the document. The elements of this tree are called DPart nodes. Each internal node contains other DPart nodes and each leaf node specifies one or more pages for a recipient. Essentially, the DPart hierarchy specifies the sequence and relationship of documents or pats of documents in a PDF/VT file. The tree structure of DPart nodes represent the internal contents of a PDF/VT document easily as it may contain sub-documents for many recipients and each document part corresponds to the pages for a single recipient. The DPart hierarchy is required in PDF/VT files.

## Document Part Metadata (DPM) ##

The Document Part Metadata (DPM) is associated with each node in the document part hierarchy and can be used to communicate information about a particular recipient's sub-document and its parts. In particular, the DPM can contain information about the properties or information about the recipients in an encoded form.

## Conformance Levels ##

PDF/VT is conferred upon the following three conformance levels. These are all based on [PDF](/pdf/) 1.6.

* `PDF/VT-1` - It is based on PDF/X-4 and contains all the resources required for rendering a PDF document.
* `PDF/VT-2` -  Designed for multi-file exchange, PDF/VT-2 documents can reference external output intents, external contents or both. A PDF/VT document and all its referenced PDF files and external output intents are collectively called a PDF/VT-2 file set. Acrobat 9 and support this feature.
* `PDF/VT-2s` -  Supports PDF/VT-2 live streaming. This allows segmented sections of data to be processed.

## References ##

* [PDF/VT - By Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Graphic Technology](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber#46428)
