{
  "date" : "2020-11-11",
  "keywords" : [ "MDF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MDF file format and APIs that can create and open MDF files.",
  "title" : "MDF File Format - SQL Server Master Database File",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is a MDF file?

A file with .mdf extension is a Master Database File used by [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) to store user data. It is of prime importance as all the data is stored in this file. The MDF file stores users data in relational databases in the form columns, rows, fields, indexes, views, and tables. SQL Server allows to set autogrow and autoshrink settings to have a positive impact on the performance of the database. MDF files can be loaded and attached to a database using Microsoft SQL Server. MDF files have Application/octet-stream mime type.

## MDF File Format

The fundamental unit of data storage in SQL Server is a page. A database assigned storage page is divided into logical pages numbering from 0 to n. A single page starts with a 96 bytes header that comprises of Page ID, type of structure that the page belongs to, number of records in the page, and pointers to the previous and next pages.

### File Structure

A MDF file has the following data structure.

 * Page 0: Header
 * Page 1: First PFS
 * Page 2: First GAM
 * Page 3: First SGAM
 * Page 4: Unused
 * Page 5: Unused
 * Page 6: First DCM
 * Page 7: First BCM

#### File Header

The page number 0 of all the files contains a header that stores metadata about the file.

#### Page Free Space (PFS)
PFS identifies the allocation status and determines the amount of free space.

 * Bit 1: Indicates whether the page is allocated or not.
 * Bit 2: Indicates if the page is from a mixed extent.
 * Bit 3: Indicates that this page is an IAM page.
 * Bit 4: Indicates that this page contains ghost records
 * Bits 5 to 7: A combined three-bit value, which indicate the page fullness as follows:
   * 0: The page is empty
   * 1: The page is 1–50% full
   * 2: The page is 51–80% full
   * 3: The page is 81–95% full
   * 4: The page is 96–100% full

## References

 * [Database Files and Filegroups](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Database Detach and Attach - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
 * [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)
