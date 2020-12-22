{
  "date" : "2020-11-11",
  "keywords" : [ "LDF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about LDF file format and APIs that can create and open LDF files.",
  "title" : "LDF File Format - SQL Server Master Database File",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is a LDF file?

A file with .ldf extension is a log file maintained by Microsoft SQL Server which is a relational database management system (RDBMS). All the transactions performed on primary database files ([MDF](/database/mdf/))(such as insertion, update, deletion) are recorded in the LDF file. LDF files are critical components of any database. In case of a system failure, the log file is used to restore the database to a consistent state. Transactions log file can increase in size if transactions are not fully committed. LDF files can be opened with Microsoft SQL Server software application.

## Operations Recorded in LDF File

An SQL log file records the following operations:

 * The start and end of each transaction.

 * Every data modification (insert, update, or delete). This includes changes by system stored procedures or data definition language (DDL) statements to any table, including system tables.

 * Every extent and page allocation or deallocation.

 * Creating or dropping a table or index.

## LDF File Format

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Since the operations are recorded in a serial, the change described by LSN2 was performed after the log record LSN1. The records for a particular transaction are linked backward using pointers that are used and speed the rollback of the transaction.


## References

 * [Database Files and Filegroups](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Database Detach and Attach - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)
