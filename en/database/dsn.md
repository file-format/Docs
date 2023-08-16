{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DSN file format and APIs that can create and open DSN files.",
  "title" : "DSN File Format - Database Source Name File",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
    }
  },
  "lastmod" : "2020-01-17"
}

## What is a DSN file?

DSN stands for "Data Source Name" and it is a file format used to store database connection information. DSN files are typically used in conjunction with ODBC (Open Database Connectivity) and allow for easy access to a specific database by providing the necessary information to connect to it, such as the server name, username, and password. The file is usually in plain text and can be created and edited using a text editor. It can be used on various operating systems like Windows, Linux and Mac.

## How to create DSN file?

The method for creating a DSN file may vary based on the operating system and the tools that are available. The following steps provide a general overview of the process for creating a DSN file on a Windows system.

1. Open the ODBC Data Source Administrator by searching for "ODBC Data Sources" in the start menu.
2. Select the "System DSN" tab and click the "Add" button.
3. Select the appropriate driver for the database you wish to connect to and click "Finish".
4. Fill in the necessary information to connect to the database, such as the server name, username, and password.
5. Click "OK" to save the DSN file.

Alternatively, you can create a DSN file manually by creating a plain text file with the .dsn extension and entering the necessary connection information in the format:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

You can then use the path of this file as the DSN in your code/script to connect to the database.

## Programs that Open DSN file

A DSN file is a plain text file that stores information used to connect to a database, such as the server name, username, and password. It is typically used in conjunction with ODBC (Open Database Connectivity) to provide easy access to a specific database.

To open and view the contents of a DSN file, you can use any text editor such as Notepad, Sublime Text, Atom, etc. These programs will allow you to open the DSN file and view the connection information stored within it.

However, to use the DSN file to connect to a database and execute operations like SELECT, INSERT, UPDATE, DELETE etc, a program with ODBC support, such as a programming language like Python, Java, C# or a database management tool like Microsoft Access, SQL Server Management Studio is required. These programs can use the information in the DSN file to connect to the database and perform the desired operation.

## References

* [What is a DSN (Data Source Name)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30-606e-2436fe26e89f)

