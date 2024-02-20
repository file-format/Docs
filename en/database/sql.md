{
  "date": "2020-11-11",
  "keywords": [
    "SQL",
    "extension",
    "file",
    "file format",
    "Database File Type",
    "Database File Format",
    "Database Files"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about SQL file format and APIs that can create and open SQL files.",
  "title": "SQL File Format - A Structured Query Language Data File",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sql"
    }
  },
  "lastmod": "2020-11-11"
}

## What is an SQL file?

A file with .sql extension is a Structured Query Language (SQL) file that contains code to work with relational databases. It is used to write SQL statements for CRUD (Create, Read, Update, and Delete) operations on databases. SQL files are common while working with desktop as well as web-based databases. There are several alternatives to SQL such as Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL, and several others. SQL files can be opened by query editors of Microsoft SQL Server, MySQL and other plain text editors such as Notepad on Windows OS.

## Brief History

* Developed and introduced by Donal D. Chamberlin and Raymond F. Boyce at IBM in early 1970s
* Used to store and retrieve data from IBM's original quasi-relational database management system, System R
* Started used in commercial products base don their System R prototype including System/38, SQL/DS, and DB2, which were commercially available in 1979, 1981, and 1983, respectively.
* Officially adopted by ANSI and ISO standard groups as standard "Database Language SQL" for relational database management systems (RDBMS) by 1986

## SQL File Format

SQL files are in plain text format and can comprise of several language elements. Multiple statements can be added to a single SQL file if their execution is possible without depending on each other. These SQL commands can be executed by query editors for carrying out CRUD operations.

### SQL Language elements

SQL language elements are as listed below.

|Element|Description|
---|---|
|Clauses| Constituent components of statements and queries.|
|Expressions| Can produce either scalar values, or tables consisting of columns and rows of data|
|Predicates| Specify conditions that can be evaluated to SQL three-valued logic (3VL) (true/false/unknown) or Boolean truth values and are used to limit the effects of statements and queries, or to change program flow.|
|Queries| Retrieve the data based on specific criteria. This is an important element of SQL.|
|Statements| May have a persistent effect on schemata and data, or may control transactions, program flow, connections, sessions, or diagnostics.|

### SQL Example
The following SQL statement creates a table named **DATA**, followed by additional `INSERT` commands to insert records in this table.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## References ##

* [SQL by Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [SQL Syntax](https://en.wikipedia.org/wiki/SQL_syntax)
