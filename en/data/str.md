{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "STR File - dBASE Structure List Object File - What is .str file and how to open it?",
  "description" : "Learn about STR dBASE Structure List Object File and how to open it.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-02-08"
}

## What is an STR file?

STR file format is commonly associated with dBASE, a database management system. In dBASE, a .str file typically represents a structure list object file. This file contains structure of a database table, including information about fields (columns) and their properties.

The structure list object file (.str) contains metadata such as field names, data types, field lengths, and any other properties associated with each field in database table. It is used to define structure of database table without containing actual data records.

Programs like dBASE or other database management tools can utilize this file to understand the layout of database table and perform operations such as querying, updating, or creating new records based on this structure.

Here is a basic example of what a STR file might contain:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

This example describes a table with four fields: ID, Name, Age, and DOB, along with their respective data types and lengths.

## How to open STR file?

The primary way to open .str files is by using dBASE itself, particularly on Windows operating systems. dBASE is capable of reading and interpreting the content of these files, allowing users to view and work with database structure.

Since .str files are essentially plain text files that contain information about structure of database, you can also open them using a text editor. Examples of text editors include Microsoft Notepad on Windows and Apple TextEdit on Mac. When opened in a text editor, you will be able to see contents of the file, including field names, data types, and other structural information, in a human-readable format.

## References
* [dBase](https://en.wikipedia.org/wiki/DBase)
