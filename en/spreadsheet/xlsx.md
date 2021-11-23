{
  "date" : "2019-12-10",
  "keywords" : [ "XLSX", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about what is an XLSX file and APIs that can create and open XLSX files.",
  "title" : "What is an XLSX file?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

## What is an XLSX file?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Based on structure organized according to the Open Packaging Conventions as outlined in [Part 2](https://www.ecma-international.org/publications/standards/Ecma-376.htm) of the OOXML standard ECMA-376, the new format is a zip package that contains a number of XML files. The underlying structure and files can be examined by simply unzipping the .xlsx file.

## Brief History

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Previous to XLSX, the common file format used was [XLS](/spreadsheet/xls/) that was pure binary file format. The new file type has added advantages of small file sizes, less changes of corruption and well-formatted images representation. It was in the early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well.

## XLSX File Format Specifications ##

The official [XLSX file format specifications](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) are available online from Microsoft. In order to see what is inside the XLSX file, just rename it to [ZIP](/compression/zip/) file by changing its extension and then extract it to view the constituent files of this Excel workbook. A blank workbook, when extracted to its files, has the following constituent files and folders.

### [Content_Types].xml ###

This is the only file that is found at the base level when the zip is extracted. It lists the content types for parts within the package. All references to the XML files included in the package are referenced in this XML file.

### \_rels (Folder) ###

This is the Relationships folder that contains a single XML file that stores the package-level relationships. Links to the key parts of the Xlsx files are contained in this file as URIs. These URIs identify the type of relationship of each key part to the package. This includes the relationship to primary office document located as xl/workbook.xml and other parts within docProps as core and extended properties.

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

## XLSX Format Example ##


For each Excel worksheet contained in a workbook, there is one XML file. You can find these XML files in xl/worksheets folder. All the information contained in a worksheet is organized in different sections in the XML file. Let's examine a sample worksheet from a workbook which is shown in the following image.

{{< figure src="../XLSX file format.png" alt="XLSX File Format" >}}

As can be seen, this worksheet contains contents in cells A1 through B2 and an image. In addition, cell G13 is currently the active cell in the worksheet. Now, let's examine the xl/worksheets/sheet1.xml file to see how this information is represented in the XML file. Contents of this XML file are as shown below.

{{< figure src="../XLSX File Format Details.png" alt="XPS File Format" >}}

1. The tab has theme color applied to it. Its mentioned in the XML file with tag <tabColor> following the theme id.
1. The tabSelected value is set to 1 which shows that this is the selected sheet
1. As can be seen in first image above, cell G13 in the worksheet is active cell which is also mentioned in the XML file.
1. The sheetData tab represents the data contained in the worksheet. However, you can see that the original contents of the worksheet are nowhere in this section. This is because the text is indirectly referred from "sharedStrings" XML sheet. This linking ensures that each text is saved only once and can be referenced again in order to save space.
1. The image as can be seen is referenced by reference id "rId2"
  
## Contribute
 
Have to share something about XLSX or Spreadsheet file formats? You can post your findings in [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet) section.

## References

* [[MS-XLSX] - XLSX File Format](https://products.conholdate.app/viewer/view/1VZC8xPx2ZuGLz2wP/ms-xlsx-excel-extensions-to-the-office-open-xml-spreadsheetml-file-format.pdf)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
