{
  "date" : "2019-12-16",
  "keywords" : [ "OTS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about OTS file format and APIs that can create and open OTS files.",
  "title" : "OTS - OpenDocument Spreadsheet Template File Format",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2021-01-19"
}

## What is an OTS file?

A file with .ots extension is an OpenDocument Spreadsheet Template file that is created with the Calc application software included in Apache OpenOffice. Calc application software is the similar to Excel available in Microsoft Office. OTS file format is used to create templates that contain predefine settings related to styles, font, data, spreadsheet layout, and formatting. OTF files have `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. These template files can be used as a starting point to generate and save actual data files that are saved in [ODS file format](/spreadsheet/ods/). OTS files can be used with applications such as OpenOffice and LibreOffice.

## OTS File Format

OTS files are saved in OASIS' OpenDocument XML-based file format that comprises of a collection of several subdocuments with a package as a [ZIP](/compression/zip/) archive. Each zip archive stores part of the complete document and each subdocument stores a particular aspect of the document. For example, one subdocument contains the style information and another subdocument contains the content of the document. A typical ODF document has the following components:

### Content.xml

The content.xml file contains the actual content of the document. This doesn't include binary data such as images, however.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml

The styles.xml file contains styling information and is heavily used for formatting and layout. Styles types include:

 * Paragraph styles
 * Page styles
 * Character styles
 * Frame styles
 * List styles

### Meta.xml

The meta.xml file contains information about the file metadata such as Author, Last Modified Date, etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

The `settings.xml` file includes document level settings such as zoom factor and cursor position.

## References ##

* [OpenDocument 1.2 specification](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
