{
  "date" : "2019-12-12",
  "keywords" : [ "SQLite", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about SQLITE file format and APIs that can create and open SQLITE files.",
  "title" : "SQLite - Database File Format",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-09"
}

## What is a SQLite File?

A file with .sqlite extension is a lightweight SQL database file created with the SQLite software. It is a database in a file itself and is used for storing data and implements a self-contained, full-featured, highly-reliable SQL database engine. SQLite database files can be used to share rich contents between systems by simple exchanging these files over the network. Almost all mobiles and computers use SQLite for storing and sharing of data, and is the choice of file format for cross-platform applications. Due to its compact use and easy usability, it comes bundled inside other applications. SQLite bindings exist for programming languages such as C, [C#](/programming/cs), [C++](/programming/cpp), Java, PHP, and many others.

## SQLite File Format

SQLite in reality is a C-Language library that implements the SQLite RDBMS using the SQLite file format. With the evolution of new devices every single day, its file format has been kept backwards compatible to accommodate older devices. SQLite file format is seen as long-term archival format for the data.

### The Database File

An SQLite database is fully maintained via two files.
 * Main database File - Contains complete state of the SQLite database
 * Rollback Journal - Stores additional information in a second file and is used during performing transactions. In case SQLite is in WAL mode, a write-head log file is maintained.

#### Journal File

This file is intended to keep all the information maintained in case the last transaction could not be completed in cases such as a computer crash. This file is used to restore the database file to a consistent state.

#### Pages

The main SQLite database file comprises of one or more pages. At any point in time, every page in the main database has a single use which is one of the following:

 * The lock-byte page
 * A freelist page
   * A freelist trunk page
   * A freelist leaf page
 * A b-tree page
   * A table b-tree interior page
   * A table b-tree leaf page
   * An index b-tree interior page
   * An index b-tree leaf page
 * A payload overflow page
 * A pointer map page

The size of SQLite database files can range from few kilobytes to few gigabytes.

### SQLite Header

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Details of the header fields are as in the following table.

|Offset|Size|Description|
---|---|---|
|0|16|The header string: "SQLite format 3\000"|
|16|2|The database page size in bytes. Must be a power of two between 512 and 32768 inclusive, or the value 1 representing a page size of 65536.|
|18|1|File format write version. 1 for legacy; 2 for WAL.|
|19|1|File format read version. 1 for legacy; 2 for WAL.|
|20|1|Bytes of unused "reserved" space at the end of each page. Usually 0.|
|21|1|Maximum embedded payload fraction. Must be 64.|
|22|1|Minimum embedded payload fraction. Must be 32.|
|23|1|Leaf payload fraction. Must be 32.|
|24|4|File change counter.|
|28|4|Size of the database file in pages. The "in-header database size".|
|32|4|Page number of the first freelist trunk page.|
|36|4|Total number of freelist pages.|
|40|4|The schema cookie.|
|44|4|The schema format number. Supported schema formats are 1, 2, 3, and 4.|
|48|4|Default page cache size.|
|52|4|The page number of the largest root b-tree page when in auto-vacuum or incremental-vacuum modes, or zero otherwise.|
|56|4|The database text encoding. A value of 1 means UTF-8. A value of 2 means UTF-16le. A value of 3 means UTF-16be.|
|60|4|The "user version" as read and set by the user_version pragma.|
|64|4|True (non-zero) for incremental-vacuum mode. False (zero) otherwise.|
|68|4|The "Application ID" set by PRAGMA application_id.|
|72|20|Reserved for expansion. Must be zero.|
|92|4|The version-valid-for number.|
|96|4|SQLITE_VERSION_NUMBER|

## References ##

* [SQLite File Format - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
