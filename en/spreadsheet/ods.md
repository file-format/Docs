{
  "date" : "2019-12-10",
  "keywords" : [ "ODS", "file", "extension", "file format", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an ODS file and APIs that can create and open them.",
  "title" : "What is a ODS file? ",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

Files with ODS extension stand for OpenDocument Spreadsheet Document format that are editable by user. Data is stored inside ODF file into rows and columns. It is XML-based format and is one of the several subtypes in the Open Document Formats (ODF) family. The format is specified as part of the ODF 1.2 specifications published and maintained by OASIS. A number of applications on Windows as well as other operating systems can open ODS files for editing and manipulation including Microsoft Excel, NeoOffice and LibreOffice. ODS files can also be converted into other spreadsheet formats as well like [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) and others by different applications.

## Brief History ##

ODS file format specifications are based on the standard developed as ODF specifications. These specifications have evolved over past in the form of three versions developed and published by OASIS as follow:

**2005: **Version 1.0 was published in May 2005

**2007: **Version 1.1 was published in Feb 2007

**2011: **Version 1.2 was published in Sep 2011

There were pretty minor changes in transition from ODF 1.0 to 1.1 versions. The [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) is the latest version for ODF specifications and should be consulted by developers for development of applications related to ODS reading/writing.

ODS File Format

OpenDocument format supports document representation as a single XML document as well as a collection of several subdocuments within a package as [ZIP](/compression/zip/) archive.  Each of the files from the ZIP archive stores part of the complete document. Each subdocument stores a particular aspect of the document. For example, one subdocument contains the style information and another subdocument contains the content of the document. A typical ODF document has the following components:

* `content.xml` – Document content and automatic styles used in the content.
* `styles.xml` – Styles used in the document content and automatic styles used in the styles themselves.
* `meta.xml` – Document meta information, such as the author or the time of the last save action.
* `settings.xml` – Application-specific settings, such as the window size or printer information.

Besides these, in package can be many other subdocuments like document thumbnail, images, etc.

Spreadsheet document files are the subset of ODF files where the content (sheets) is stored in //content.xml// subdocument.

## References ##

* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
