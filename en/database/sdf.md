{
  "date" : "2021-05-03",
  "keywords" : [ "SDF", "sdf file","what is sdf file","how to open an sdf file", "extension", "file", "sdf file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about SDF file format and APIs that can create and open SDF files.",
  "title" : "SDF - SQL Server Compact Database File",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-05-03"
}

## What is an SDF file?
A file with .sdf extension contains the Microsoft SQL Server Compact (SQL CE) database which is also known as a compact relational database; produced by Microsoft for the applications made for mobile devices and desktops. It supports both 32 and 64 bits operating system and the complete content of database is included in a single SDF file and can occupy more than 4GB disk space. For the security purpose, a .sdf file can be encrypted with 128-bit encryption. The SQL CE runtime settles parallel multi-user access to the .sdf file. The SDF file can be copied via **QuickOnce** or simply it can be copied to destination for system deployment.

## SDF file format
An SDF file contains a database which is usually called compact relational database. An SDF file contains all the database related information and the SQL Server Compact is a light weight and free database engine which is used to manage the .sdf files. The .sdf file size shouldn't exceed the limit of 4 GB of size. The SDF files don't store the information about stored procedures, triggers or views. Applications using an SQL CE database need not specify the path to an SDF file in the ADO.NET connection string, instead it can be mentioned as |DataDirectory|\database_name.sdf, defining the data directory being defined in the assembly manifest for the application
The .sdf naming convention is optional, and any extension can be used to save the file. Setting up a password for the database file is an optional step. To compress or repair the database the file should be saved with the option of the **compacted/repaired database**.

## How to open an SDF file?
 The SQL Server Management Studio or SQL Server Data Tools (the SQL Server Object Explorer window in Visual Studio) are not capable to manage SQL Server Compact databases, but other options like following are available:
 - Server Explorer in Microsoft Visual Studio offers limited database manipulation functionality.
 - The Databases tab in WebMatrix has more features than Server Explorer.
 - Relatively full-featured third-party or open source tools are available

### Softwares that can open the SDF files ###
The SDF files can be opened in the following softwares:

|Software| Operating System|
---|---|
|Microsoft SQL Server 2019|Microsoft Windows|
|Microsoft Visual Studio 2019|Microsoft Windows|
|LINQPad|Microsoft Windows|


## References

 * [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [Using SQL Server Compact for ASP.NET Web Applications](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))

