{
  "date" : "2020-11-11",
  "keywords" : [ "NDF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MDF file format and APIs that can create and open NDF files.",
  "title" : "NDF File Format - SQL Server Master Database File",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is a NDF file?

A file wiht .ndf extension is a secondary database file used by [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) to store user data. NDF is secondary storage file because SQL server stores user specified data in primary storage file known as [MDF](/database/mdf/). NDF data file is optional and is user-defined to manage data storage in case the primary MDF file uses all the allocated space. It is usually stored on separate disk and can spread to multiple storage devices. The presence of MDF files is necessary in order to open NDF files.

## NDF File Format

NDF file format is no different than [MDF](/database/mdf/) and uses pages as the fundamental unit of data storage. each page starts with 96 bytes header that includes:

 * Page ID
 * Type of Structure
 * Number of records in the pages
 * Pointers to previous and next pages

### NDF File Structure

A MDF file has the following data structure.

 * Page 0: Header
 * Page 1: First PFS
 * Page 2: First GAM
 * Page 3: First SGAM
 * Page 4: Unused
 * Page 5: Unused
 * Page 6: First DCM
 * Page 7: First BCM

#### NDF File Header

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

## Data File Page

Pages in a SQL Server data file start from zero (0) and increment sequentially. Each file is recognized by a unique file ID number. The file ID and page number pair uniquely identifies a page in a database. An example showing page numbers in a database, is as in following image.

{{< figure src="../ndf.png" alt="NDF Database File Format" >}}

This example shows page numbers in a database that has a 4-MB primary data file and 1-MB secondary data file.

## References

 * [Database Files and Filegroups](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
 * [Database Detach and Attach - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
 * [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)
