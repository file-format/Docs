{
  "date" : "2021-02-26",
  "keywords" : [ "SXC", "file", "extension", "file format", "Sun XML Calc", "Spreadsheet" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about SXC file format and APIs that can create and open SXC files.",
  "title" : "SXC File Format",
  "linktitle" : "SXC",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2021-02-26"
}

## What is a SXC file? ##

The file format SXC(Sun XML Calc) belongs to an office suite called OpenOffice.org. This format generally deals with the spreadsheet needs of users as it is an XML based spreadsheet file format. SXC format supports formulas, functions, macros and charts along with DataPilot, which is an incredible feature because it automatically individualizes and provides summaries of raw imported data. The files created with this software are saved with extension .sxc.


## SXC File Format ##

Files, having extensions .sxc, can be opened with Microsoft excel which is a spreadsheet software from Microsoft Office suite. There are other software which can open files with .sxc extension i.e. Libre Office, StarOffice etc. 

The content type for this format are:

* application/vnd.sun.xml.calc
* application/vnd.sun.xml.calc.template

## File Compatibility ##

SXC files are compatible with Apache Open Office calc and data can be exported to Microsoft excel file and other formats as well.

## File Handling ##

The commands ImportMatrix and ExportMatrix can read and write SXC file. When the source is a SXC file and target is also a SXC file, it causes **f** to be considered as Sun XML Calc Spreadsheet file. Both Import and Export Matrix support this format, which is auto detected when the format is unspecified and the filename ends in .sxc.

In order to open SXC file, an appropriate program is required to be associated to the file. Whenever a file with extension .sxc is to be opened, make sure its error free and it is not corrupted. Any error in the file can be easily handled by the user and this does not require a technical support most of the times.


## References ##

* [StarOffice - By Wikipedia](https://en.wikipedia.org/wiki/StarOffice)
