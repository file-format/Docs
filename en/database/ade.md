{
  "date" : "2021-08-29",
  "keywords" : [ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ADE file format and APIs that can create and open ADE files.",
  "title" : "ADE - Access Project Extension File",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-08-29"
}

## What is an ADE file?

A file with .ade extension is a Microsoft Access Project file that contains the compiled output of the information contained in the Microsoft Access ADP project file. Information in the Access project file, other than Visual Basic for Applications (VBA), is available in compiled form in ADE files. Data is stored in compressed format in these files to reduce the file size and improve performance in Access. Since ADE is the compiled output of the Access project file, any VBA source code which is part of the project, remains protected by not allowing it to be part of the output. ADE files can be opened in Microsoft Access 365.

## ADE File Format - More Information

ADE are compiled Access Database files that are stored to disc as binary files. The internal file structure of these files are not known.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. This issue occurs because Access 2010 SP1 uses a newer version of the VBE7.dll file (version 7.00.1619).

## References

* [Issue with Access ADE Files](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Which Access File Formats to Use](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
