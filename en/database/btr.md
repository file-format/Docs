{
  "date" : "2021-09-06",
  "keywords" : [ "btr", "extension", "file", "file format", "Database File Type", "Database File Format", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about BTR file format and APIs that can create and open BTR files.",
  "title" : "BTR - Btrieve Database File",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-09-06"
}

## What is an BTR file?

A file with .btr extension is a database file created by [Btrieve](https://www.actian.com/) transactional database application. Unlike relational database management systems (RBMS),  Btrieve is based on Indexed Sequential Access Method (ISAM), which is a way of storing data for fast retrieval. The BTR file stores a collection of records and is used to generate reports as per requirements. BTR files can be opened using Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility, and Legend Software BTRIEVE Viewer.

## BTR File Structure - More Information

The internal data structure and alignment of each byte in the structure of a BTR file is not publicly available. However, Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * GNU C/C++
 * Micro Focus COBOL
 * Microsoft Visual Basic
 * Microsoft Visual C++
 * Watcom C/C++

Retrieving data from a BTR file is dependent on the associated DDF file with it. Without the DDF, it won't be easy to retrieve the information from such a file.

## References

* [Betrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)
