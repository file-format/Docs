{
  "date": "2019-10-11",
  "keywords": [
    "xoml",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "Extensible Object Markup Language"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XOML - Windows Workflow File Format",
  "description": "Learn about XOML file format and APIs that can create and open XOML files.",
  "linktitle": "XOML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xoml"
    }
  },
  "lastmod": "2019-09-10"
}

## What is an XOML file?

XOML is acronym for Extensible Object Markup Language and is a serialization format for Windows Workflow Foundation's workflow objects. Based on **[XAML](/web/xaml/)**, it is mostly used for creating user interfaces in plain **[XML](/web/xml/)**. These are used to declare the workflow for user interface and are compiled along with the separate file containing implementation logic. It contains a tree based structure that defines a root workflow node, nested sub-elements and embedded segments of code. When a new workflow is created with Visual Studio for .NET, it has an option for you to choose whether it should be in Code format or Code Separated format. In case you select the later one, the IDE will create two files for you; one in XOML format (consisting of workflow layout and settings), and other is in [.CS](/programming/cs/)/[.VB](/programming/vb/) format where the programming code resides.
