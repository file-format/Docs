{
  "date" : "2019-12-10",
  "keywords" : [ "\_XLSX", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an XLSX file and APIs that can create and open them.",
  "title" : "What is an \_XLSX file?",
  "linktitle" : "\_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

## What is a \_XLSX file?

A file with .\_xlsx extension is actually an [XLSX](/spreadsheet/xlsx/) file that is renamed by some other application. This can happen in certain cases when the filename contains a . at the end of the file name. The \_XLSX files can be opeend in Microsoft Excel similar to the XLSX files by again renaming these to .xlsx extension.

## \_XLSX File Format - More information

The \_XLSX files are no difference than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Before XLSX, [XLS](/spreadsheet/xls/) was the primary file format used for working with Excel spreadsheets to save documents in binary format. This new XML based file format came with advantages such as small file sizes, resistance to file corruption, and well-formatted images representation. This new XML based file format became part of Office 2007 and is carried out in the new versions of Microsoft as well.

## \_XLSX File Format Specifications

As an \_XLSX file is an XLSX file renamed, it has the same specifications as the original file. It is an archive file that is based on the [ZIP](/compression/zip/) archival file format. If you want to see the contents of this archive, just rename the file to .zip extension and extract it to view the constituent files of this Excel workbook. A blank workbook, when extracted to its files, has the following constituent files and folders.

### [Content_Types].xml

This is the only file that is found at the base level when the zip is extracted. It lists the content types for parts within the package. All references to the XML files included in the package are referenced in this XML file.

### \_rels (Folder)

This is the Relationships folder that contains a single XML file that stores the package-level relationships. Links to the key parts of the Xlsx files are contained in this file as URIs. These URIs identify the type of relationship of each key part to the package. This includes the relationship to primary office document located as xl/workbook.xml and other parts within docProps as core and extended properties.

### docProps

This folder contains the overall document properties. These include a set of core properties, a set of extended or application-specific properties and a thumbnail preview of the document. A blank workbook has two files in this folder namely app.xml and core.xml. The core.xml contains information like author, date created and saved, and modified. App.xml contains information about the content of the file.

### xl (Folder)

This is the main folder that contains all the details about the contents of the workbook. By default, it has following folders:

* \_rels
* theme
* worksheets

and following xml files:

* styles.xml
* workbook.xml

## References

* [[MS-XLSX] - .xlsx File Format](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
