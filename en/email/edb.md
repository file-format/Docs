{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EDB File Format - An Exchange Mail Database File",
  "description":"Learn about EDB file format and APIs that can create and open EDB files.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2020-09-16"
}

## What is an EDB file?

A file with .edb file extension is mailbox database created by Microsoft Exchange Server to store mail-related data. EDB, Exchange Database, stores messages that are in-process and non-SMTP. EDB are also known as Extensible Storage Engine (ESE) Database files and store files using b-tree structure. Being storage files, EDB files can be converted into other mail storage file formats such as [PST](/email/pst/) and [OST](/email/ost/).

## EDB File Format

There is no official/open EDB file format specifications available that can be referenced. Some progress has been made for reverse engineering the file format, resulting in partial specifications decoding. As per these, an EDB file consists of:
 * File Header - Contains database file header information
 * Fixed Size Pages - Contains the database which consits of tables and indexes

### Database File Header
The database file header resides in the first database page and is atleast 668 bytes. The file header contains `File Format Version` and `File Type` in addition to other fields.

#### File Types
|Type|Description
---|---|
|0| Database|
|1| Streaming|

`Note:` Identifiers for these types are not known.

#### File Format Version
The original format of EDB started in April 1997 and kept evolving for changes thereafter.

|Revsion Date|Version|Revision|description
---|---|---|---|
|Apr 1997| 0x00000620|0x00000000| Original operating system Beta format.|
|May 1997 |0x00000620|0x00000001| Add columns in the catalog for conditional indexing and OLD.|
|Jun 1997|0x00000620|0x00000002|Add the fLocalizedText flag in IDB.|
|Oct 1997|0x00000620|0x00000003|Add SPLIT_BUFFER to space tree root pages.|
|Jan 1998|0x00000620|0x00000002|Revert revision in order for ESE97 to remain forward-compatible.|
||0x00000620|0x00000003|Add new tagged columns to catalog ("CallbackData" and "CallbackDependencies").|
|May 1998|0x00000620|0x00000004|Super Long Value (SLV) support: signSLV, fSLVExists in dbheader.|
|May 1998|0x00000620|0x00000005|New SLV space tree.|
|Oct 1998|0x00000620|0x00000006|SLV space map.|
|Dec 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Jan 1999|0x00000620|0x00000008|New template column format.|
|Jun 1999|0x00000620|0x00000009|Sorted template columns. Used in Windows XP SP3|
||0x00000620|0x0000000b|Contains the page header with the ECC checksumUsed in Exchange|
||0x00000620|0x0000000c|Used in Windows Vista (SP0)|
||0x00000620|0x00000011|Support for 2 KiB, 16 KiB and 32 KiB pages.Extended page header with additional ECC checksums.Column compression.Space hints.Used in Windows 7 (SP0)|
|May 1999|0x00000623|0x00000000|New Space Manager.|

### Database Files

The EDB database file contains the schema for all the tables in the database. In addition, it also includes records for all database tables and indexes for the tables. Its location is determined by the following identifiers.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Based on these, the state of the database can be assessed as follow.

|Value|Identifier|Description
---|---|---|
|1|JET_dbstateJustCreated|The database was just created.|
|2|JET_dbstateDirtyShutdown|The database requires hard or soft recovery to be run in order to become usable or movable. One should not try to move databases in this state.|
|3|JET_dbstateCleanShutdown|The database is in a clean state. The database can be attached without any log files.|
|4|JET_dbstateBeingConverted|The database is being upgraded.|
|5|JET_dbstateForceDetachInternal|This value is introduced in WindowsXP|
 
## References
 * [Extensible Storage Engine (ESE) Database File (EDB) Specifications](https://github.com/libyal/libesedb/tree/master/documentation)
