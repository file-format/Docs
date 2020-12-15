{
  "date" : "2020-11-11",
  "keywords" : [ "NSF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about NSF file format and APIs that can create and open NSF files.",
  "title" : "NSF File Format - Lotus Notes Database Format",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is an NSF file?

A file with .nsf (Notes Storage Facility) extension is a database file format used by the [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino), which was previously known as Lotus Notes. It defines the schema to store different kind of objects such like emails, appointments, documents, forms and views. All this information is contained in a single NSF file for business collaboration similar to a PST/OST file. Some of the applications that can open NSF files include IBM Lotus Notes and IBM Domino.

## NSF File Format Specifications

NSF files are binary in nature and their specifications are available by Joachim Metz on [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). As per these details, an NSF file comprises of:

 * File Header
 * Database Header

 In addition, it consists of:

 * Superblock
 * Bucket descriptor block
 * Bitmap
 * Record Relocation Vector bucket
 * Summary buckets
 * Non-summary buckets


### NSF File Header

The NSF file header is a 6 bytes in size. It consists of:

|Offset|Size|Value|Description|
---|---|---|---|
0|2|0x1a 0x00|Signature|
2|4| |The database header size|

### Database header

The NSD Database header contains the following confirmed values.

 * Database Information
   * Database identifier (DBID)
 * Replication information
 * Database information buffer flags
   * Title
   * Categories
   * Class
   * Design class (template name)
 * Special note identifiers
 * Padding
 * Database information 2
 * Database information 3
 * Database information 4
 * Database information 5
 * Padding
 * Database instance identifier (DBIID)
 * Replication history
## References

 * [NSF Format - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)
