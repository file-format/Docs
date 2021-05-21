{
  "date" : "2020-11-11",
  "keywords" : [ "DDL", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DDL file format and APIs that can create and open DDL files.",
  "title" : "DDL File Format - A Data Definition Language File",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-11"
}

## What is an DDL file?

A file with .ddl extension is a Data Definition Language file that is used to define the schema of a database. It contains statements/commands for working with database structures such as tables, columns, records, and other fields. Commands in a DDL file are written in [SQL](/database/sql/) and can perform operations such as create table in database, drop and update. A database schema is owned by its created and all the CRUD operations can be performed on it. Popular applications that can create and open DDL files are Windows Text Editor, Jetbrains Intellij Idea, and EclipseLink.

## DDL commands

A single DDL file can contain several commands that, owing to correct syntax, will execute in sequence and make changes to the schema such as creating character sets and tables, dropping tables, renaming and altering tables. Following DDL commands are commonly used while working with database schema.

`CREATE` - Used to create the database or its objects (like table, index, function, views, store procedure and triggers).

`DROP` –  Used to delete objects from the database.

`ALTER` - Used to alter the structure of the database.

`TRUNCATE` – Used to remove all records from a table, including all spaces allocated for the records are removed.

`COMMENT` – Adds comments to the data dictionary.

`RENAME` – Renames an existing object in the database.

## DDL Example

The following example shows DDL statement for CREATE command which creates a table and defines its fields.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## References ##

* [DDL by Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)
* [DDL Commands](https://oracletutorial.net/dml-ddl-commands-in-oracle.html#ddl-commands-in-oracle)
