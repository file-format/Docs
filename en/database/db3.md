{
  "date" : "2019-12-12",
  "keywords" : [ "DB3", "DB3 File Format", "DB3 File","SQLite", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DB3 file format and APIs that can create and open DB3 files.",
  "title" : "DB3 File Format",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-09"
}

## What is a DB3 File?
The DB3 file is a database file created by the SQLite software which is a lightweight, self-contained database program that creates databases using plain files; contains the database anatomy as well as data records; commonly used for retrieving or storing structured data using SQL. These files can be used in smart devices or where the record keeping or other data management required but on a low space environment.


## DB3 File Format
The DB3 file format is associated with RDBMS (Relational Database Management System) SQLite, a popular choice for embedded database. There is no any specific file extension defined in an SQLite_3  in its specification, it may use extensions including [.dbf](/database/dbf/) and [.sqlite](/database/sqlite/). 

### The Database Secification
Commonly SQLite, version 3 related db file format can be considered as the DB3 file format used as the publicly documented native format for the SQLite database engine since June 2004. The DB3 file format, is a cross-platform, transferable between between big-endian and little-endian architectures or 32-bit and 64-bit systems. These features make DB3 a popular choice as an application file format. The main SQLite_3 database (DB3) file consists of one or more pages. All sizes of all pages are equal in same database. The page size in bytes is a power of two between 512 and 65536 inclusive.



## References ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite, Version 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)
