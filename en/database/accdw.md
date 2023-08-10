{
  "date" : "2021-08-30",
  "keywords" : [ "ACCDW", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ACCDW file format and APIs that can create and open ACCDW files.",
  "title" : "ACCDW - Microsoft Access Database Link File",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-08-30"
}

## What is an ACCDW file?

A file wiht .accdw extension is a link file created with Microsoft Access and contains information about the link to download an Access database file i.e. [ACCDB](/database/accdb/) from SharePoint server. This lets the users to share database files that are hosted remotely. Opening the ACCDW file downloads the linked ACCDB file as a local copy on the user's computer. The downloaded file is saved to the default download location and can be accessed by navigating to it. Usually, these files are downloaded and stored with the name "SiteServer.accdb" that refers to the client databases.

## ACCDW File Format - More Information

The ACCDW file is an XML file that provide a link to the SharePoint site where the Access Services are hosted. It is a shortcut only and requires internet connection to run them. In case of online, the SharePoint is cached locally in order to provide the option to take it offline later.

## References

* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Downloading .accdw file](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file?forum=sharepointgeneralprevious)
* [Which Access file format should I use?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
