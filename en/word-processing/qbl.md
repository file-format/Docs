{
  "date": "2021-07-28",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QBL - QuickBooks License File",
  "description": "Learn about QBL file format and APIs that can create and open QBL files.",
  "linktitle": "QBL",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-qbl"
    }
  },
  "lastmod": "2021-07-28"
}

## What is a QBL file?

A file with .qbl extension is a QuickBooks license file that contains licensing information for the user's purchased copy. It is usually stored in local system with the name `license.qbl` after QuickBooks is installed and user enters the licensing information in the software when software is run for the first time. QBL was the earlier file format used for storing QuickBooks licensing information. This has now been replaced by the QuickBooks `qbregisteration.dat` file and is populated with information from user's confirmation email, purchased DVD, or through other buying means. QBL files can be opened in any text editors such as Windows Notepad, Apple TextEdit, Notepad++, Github Atom editor, and many more.

## QBL File Format - More Information

QBL files are created and stored as plain text files. Information in these files is human readable and can be edited/updated when these files are opened in text editors. Licensing and user registration information can then be copied in this file for getting started with the QuickBooks software. QBL files are usually stored in the Program Files\Intuit\QuickBooks\INET directory on Windows Operating System.

A QBL file contains two types of information.

* `QuickBooks Version Information:` Referred to the installed version of QuickBooks and is in format such as xx.x
* `License Key:` Text in 000-000 0000-0000-0000-000 000073adbf3f format where 000-000 0000-0000-0000-000 is replaced with user's qbregisteration Key

## References

 * [QuickBooks by Intuit](https://quickbooks.intuit.com/)
 * [QuickBooks - Generating the qbregistration.dat file](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)
