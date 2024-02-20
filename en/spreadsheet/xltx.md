{
  "date": "2019-12-10",
  "keywords": [
    "XLTX",
    "file",
    "extension",
    "file format",
    "Excel Open XML",
    "Spreadsheet"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Your file format guide to know what is an XLTX file and APIs that can create and open them.",
  "title": "What is an XLTX file?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xltx"
    }
  },
  "lastmod": "2019-12-10"
}

## What is an XLTX file?

Files with .xltx extension represent Microsoft Excel Template files that are based on the Office OpenXML file format specifications. It is used to create a standard template file that can be utilized to generate [XLSX](/spreadsheet/xlsx/) files that exhibit the same settings as specified in the XLTX file.

## Brief History

It was in the early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents, of different types, under this new Standard were identified by appending "X" in their extensions, where "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, less changes of corruption and well formatted images representation.

## XLTX File Format Specifications

XLTX files are based on the Office OpenXML file format and use XML and [ZIP](/compression/zip/) to reduce file size. It was created with the release of Microsoft Office 2007 to replace the binary XLT file format. Similar to XLTX, the XLT file format can be used to create [XLS](/spreadsheet/xls/) files using Microsoft Excel 2003 and 2007.  These can be opened with Microsoft Excel by double clicking the file. The files organization in an XLTX file format can be observed by renaming the  file to ZIP and then extracting its contents to disc.

### [Content_Types].xml ###

This is the only file that is found at the base level when the zip is extracted. It lists the content types for parts within the package. All references to the XML files included in the package are referenced in this XML file.

### \_rels (Folder) ###

This is the Relationships folder that contains a single XML file that stores the package-level relationships. Links to the key parts of the Xltx files are contained in this file as URIs. These URIs identify the type of relationship of each key part to the package. This includes the relationship to primary office document located as xl/workbook.xml and other parts within docProps as core adn extended properties.

### docProps ###

This folder contains the overall document properties. These include a set of core properties, a set of extended or application-specific properties and a thumbnail preview of the document. A blank workbook has two files in this folder namely app.xml and core.xml. The core.xml contains information like author, date created and saved, and modified. App.xml contains information about the content of the file.

### xl (Folder) ###

This is the main folder that contains all the details about the contents of the workbook. By default, it has following folders:

* \_rels
* theme
* worksheets

and following xml files:

* styles.xml
* workbook.xml

## References ##

* [[MS-XLSX] - .Xlsx File Format](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
