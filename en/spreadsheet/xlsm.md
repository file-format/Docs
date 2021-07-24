{
  "date" : "2019-12-10",
  "keywords" : [ "XLSM", "file", "extension", "file format", "Excel Macros", "Open" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an XLSM file and APIs that can create and open them.",
  "title" : "What is an XLSM file?",
  "linktitle" : "XLSM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

## What is an XLSM file?

Files with XLSM extension is a type of Spreadsheet files that support Macros. From application point of view, a Macro is set of instructions that are used for automating processes. A macro is used to record the steps that are performed repeatedly and facilitates performing the actions by running the macro again. Macros are programmed with Microsoft's Visual Basic for Applications (VBA) from within the Excel Workbook using the Visual Basic Editor and can be run/debug directly from there.

XLSM files are similar to XLM file formats but are based on the Open XML format introduced in Microsoft Office 2007. In other words, XLSM are [XLSX](/spreadsheet/xlsx/) files but with support of macros. By default, Excel itself provides several macros for common use. However, you can also record your own macros with required functions.

## XLSM - Recording a Macro ##

Excel provides easy to use steps for recording a macro. It requires you have Developer tools installed in order to work with Macros. Once a macro recording is in process, it records each user action to be played later on. Macro recording actually involves all the steps a user performs after the recording starts. Thus, if you make a cell's content bold, italic and set its text justification after a macro recording has been started, all these commands will be recorded. Each recorded macro can be assigned a shortcut as well for quick playback later on. Macro recording generates VBA code in the form of a macro that can be edited using the Visual Basic Editor (VBE).

## References ##

* [MS-XLSX File Format](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
