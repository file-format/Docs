{
  "date" : "2020-11-11",
  "keywords" : [ "ACCDB", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ACCDB file format and APIs that can create and open ACCDB files.",
  "title" : "ACCDB File Format - Microsoft Access 2007 Database File",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-12"
}

## What is an ACCDB file?

A file with .accdb extension is a Microsoft Access 2007 database file that stores users data in tables. It supports storing
custom forms, SQL queries, and other data. ACCDB files replaced .mdb files after Microsoft shifted to XML based file structure. ACCDB files can still be converted to MDB with old compatibility. However, the ACCDB are the widely used Access database file format now. Microsoft also supported additional features in ACCDB format such as possibility of storing file attachments, binary data, and multi-valued field support.

## ACCDB File Format

Like MDB, there are no public specifications available for ACCDB file format. Microsoft supports accessing these files programatically via Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA).

### An Insight

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. In ACCDB files, this indicator appears to reflect compatibility of the file rather than the version of the ACE engine used to create it.

## References ##

* [Access File Format](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=%252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Which Access file format should I use?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
