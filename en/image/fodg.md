{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FODG - OpenDocument Drawing File Format",
  "description":"Learn about FODG file format and APIs that can create and open FODG files.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an FODG file?

A file with .fodg extension is an Apache OpenOffice Drawing file format for storing drawing elements. It is based on the file format specifications outlined by Advancement of Structural Information Standards (OASIS). Another similar file format for OpenOffice graphics is [ODG](/image/odg/) that stores drawing elements as a vector image. FODG files can be opened with OpenOffice as well as LibreOffice. Other file formats supported by OpenOffice, for example, include [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) and [ODS](/spreadsheet/ods/).

## FODG File Format Specifications

FODG is based on the OpenDocument's XML file format that conforms to OASIS OpenDocument Format ISO/IEC 26300. It has Internet Media Type application/vnd.oasis.opendocument.graphics and also conforms to org.oasis-open.opendocument public.composite-content.  The XML structure is common for all document types such as spreadsheet, drawing files, and text documents. OpenOffice documents take advantage of separation of concerns by separating the content, styles, metadata, and application settings into four separate XML files.

`<office:document-content>` - Document content and automatic styles used in the content.
`<office:document-styles>` - Styles used in the document content and automatic styles used in the styles themselves.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings>` - Application-specific settings, such as the window size or printer information.

## References ##
 * [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
 * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
 * [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
