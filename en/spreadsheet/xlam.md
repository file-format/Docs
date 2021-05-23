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

XLAM is an Macro-Enabled Add-In file that is used to add new functions to spreadsheets. An Add-In is a supplemental program that runs additional code and provides additional functionality for spreadsheets. XLAM files are stored with the .xlam extension. XLAM files are XML-based files similar to [XLSM](/spreadsheet/xlsm/) and [XLSX](/spreadsheet/xlsx/) file formats and are saved with ZIP compression to reduce the overall file size.

### Example ###

```cmd
Public Function Add(num1 As Double, num2 As Double)
Add = num1 + num2
End Function
```

After this, save the file with the .xlam extension.

## References ##

- [File format reference - ](https://docs.microsoft.com/en-us/deployoffice/compat/office-file-format-reference)
