{
  "date" : "2020-11-11",
  "keywords" : [ "MDB", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MDB file format and APIs that can create and open MDB files.",
  "title" : "MDB File Format - A Microsoft Access Database File",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-11"
}

## What is a MDB file?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. The lateral versions of Microsoft Access use the [ACCDB](/database/accdb/) file formats which is the latest file format to date. MDB files can be opened with applications like Microsoft Access, MDB Viewer, MDBOpener, and can be converted to ACCDB, [CSV](/spreadsheet/csv/), Excel formats, etc.

## MDB File Format

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Pages

As per the unofficial MDB guide, an MDB file consists of fixed-size pages (2048 bytes for Jeb DB3 and 4096 bytes for Jet DB 4). The first byte indicates the type of page. Following are the key page types:

`First Page:` It contains database header information that also includes the identification of the Jet DB version with which the file is compatible. In addition, it also includes file security information and a map of page usage.

`Table definition page:` A table definition page specifies columns, data types, index, and other information. It uses additional pages if required and includes a map of pages that contains the row data for this table.

`Data pages:` The data pages are the actual data containers where data is stored by rows. It uses subsidiary pages to store long data values.

A single Microsoft Access database may comprise of multiple files that allow to exceed file and table size limitations. This facilitates to put forms and code in a front-end MDB file on user's desktop and data in another backend MDB files on servers connected to network.

## How to open MDB file?

MDB files can be opened using the following programs.

 * Microsoft Access 365
 * Microsoft Visual Studio 2019

## References ##

* [Access Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [The Unofficial MDB Guide](http://jabakobob.net/mdb/)
