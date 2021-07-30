{
  "date" : "2019-10-11",
  "keywords" : [ "odt file", "odt file format", "what is an odt file", "file", "odt example", "odt file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ODT - OpenDocument Text File",
  "description":"Learn about ODT file format and APIs that can create and open ODT files.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an ODT file?

ODT files are type of documents created with word processing applications that are based on OpenDocument Text File format. These are created with word processor applications such as free OpenOffice Writer and can hold content such as text, images, objects and styles. The ODT file is to Writer word processor what the [DOCX](/word-processing/docx/) is to Microsoft Word. Several applications including Google Docs and Google's web-based word processor included with Google Drive can open the ODT files for editing. Microsoft Word can also open ODT files and save it in to other formats such as [DOC](/word-processing/doc/) and DOCX.

## Brief History ##

ODP file format specifications are based on the standard developed as ODF specifications. These specifications have evolved over past in the form of three versions developed and published by OASIS as follow:

**2005** Version 1.0 was published in May 2005

**2007:** Version 1.1 was published in Feb 2007

**2011:** Version 1.2 was published in Sep 2011

There were pretty minor changes in transition from ODF 1.0 to 1.1 versions. The [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) is the latest version for ODF specifications and should be consulted by developers for development of applications related to ODS reading/writing.

## File Format Specifications ##

OpenDocument format supports document representation as a single XML document as well as a collection of several subdocuments within a package as [ZIP](/Compression/ZIP/) archive.  Each of the files from the ZIP archive stores part of the complete document. Each subdocument stores a particular aspect of the document. For example, one subdocument contains the style information and another subdocument contains the content of the document. A typical ODF document has the following components:

* content.xml – Document content and automatic styles used in the content.
* styles.xml – Styles used in the document content and automatic styles used in the styles themselves.
* meta.xml – Document meta information, such as the author or the time of the last save action.
* settings.xml – Application-specific settings, such as the window size or printer information.

Besides these, in package can be many other subdocuments like document thumbnail, images, etc. Document files are the subset of ODF files where the content (sheets) is stored in //content.xml// subdocument.

## References ##

* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
