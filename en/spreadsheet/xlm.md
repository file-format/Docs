{
  "date" : "2019-12-10",
  "keywords" : [ "XLM", "file", "extension", "file format", "Microsoft Excel Macro File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an XLM Macros file and APIs that can create and open XLM files.",
  "title" : "What is an XLM file?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

## What is an XLM file?

XLM, for Excel Macro, is a type of Spreadsheet files that are used to store Macros. From application point of view, a Macro is set of instructions that are used for automating processes. A macro is used to record the steps that are performed repeatedly for [XLS](/spreadsheet/xls/) file format and facilitates performing the actions by running the macro again. Macros are programmed with Microsoft's Visual Basic for Applications (VBA) from within the Excel Workbook using the Visual Basic Editor and can be run/debug directly from there.

## Brief History ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 recorded macros in VBA by default but with version 5.0 XLM recording was still allowed as an option. After version 5.0 that option was discontinued. All versions of Excel, including Excel 2010 are capable of running an XLM macro, though Microsoft discourages their use.

## Recording a Macro in XLM ##

Excel provides easy to use steps for recording a macro. It requires you have Developer tools installed in order to work with Macros. Once a macro recording is in process, it records each user action to be played later on. Macro recording actually involves all the steps a user performs after the recording starts. Thus, if you make a cell's content bold, italic and set its text justification after a macro recording has been started, all these commands will be recorded. Each recorded macro can be assigned a shortcut as well for quick playback later on. Macro recording generates VBA code in the form of a macro that can be edited using the Visual Basic Editor (VBE).

## Excel Object Model ##

Macros use VBA routines at their back and follow the [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) for this purpose. This model identifies the objects of a spreadsheet for interaction with the spreadsheet through user-defined command toolbars, command bars or messages boxes. For example, access to the workbook's properties is granted with the Workbook object. Similarly, there is Worksheet object in the model to work with the worksheets of workbook programmatically.

## Macros and Security ##

VBA allows access to all areas of application as well as file system and can be hazardous as well. This raises concerns when sharing workbook with someone who can run the file at his end. That is Microsoft Excel warns about opening such a file. Macros can be certified with a digital signature in order for other users to verify that these are trustworthy. Thus, macros can be enabled after verification of their source.

## References ##

* [[MS-XLS] - Excel Binary File Format Structure](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Macro Programming](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)
