---
date: 2019-12-10
keywords: xlam, .xlam, xlam file format, .xlam file format, .xlam extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about XLAM file format and APIs that can create and open XLAM files.
title: XLAM File Format
linktitle: XLAM
menu:
  docs:
    parent: "spreadsheet"
lastmod: 2021-06-01
---

## What is an XLAM file? ##

XLAM is an Excel Macro-Enabled Add-In file that is used to add new functions to Excel. An Add-In is a supplemental program that runs additional code and provides additional functionality for Excel spreadsheets. XLAM files are stored with the .xlam extension. XLAM files are XML-based files similar to [XLSM](/spreadsheet/xlsm/) and [XLSX](/spreadsheet/xlsx/) file formats and are saved with ZIP compression to reduce the overall file size.

## How to create XLAM files ##

Inside Excel, use the Alt + F11 shortcut to open VB Editor. Add the code that you want to add. A simple example can be an Add function as shown below.

```cmd
Public Function Add(num1 As Double, num2 As Double)
Add = num1 + num2
End Function
```

After this, save the file with the .xlam extension.

## How to open XLAM files ##

To add the function from the XLAM file, open Excel. Go to *File > Options > Add-ins* and click the **Go** button with "Excel Add-ins" selected in the manage dropdown. Click Browse and select the XLAM file. After that, click OK.

Now you can use the newly added function in your excel files.

## References ##

- [File format reference for Word, Excel, and PowerPoint](https://docs.microsoft.com/en-us/deployoffice/compat/office-file-format-reference)
- [How to Create and Use an Excel Add-in](https://trumpexcel.com/excel-add-in/)
- [XLAM](https://filext.com/file-extension/XLAM)
