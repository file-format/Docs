{
  "date": "2021-08-24",
  "keywords": [
    "wdb file",
    "wdb file format",
    "what is a wdb file",
    "file",
    "wdb example",
    "wdb file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about WDB file format and APIs that can create and open WDB files.",
  "title": "WDB - SQL Server Trace File",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wdb"
    }
  },
  "lastmod": "2021-08-24"
}

## What is a WDB file?
A file with .wdb extension is actually a database file created by Microsoft Works which was used to perform functions like a database management system. The WDB file is similar as the Access Database ([MDB](/database/mdb/)) file, but less efficient and greater limitations. The WDB files can't be opened by using Microsoft Access. However, you can open the WDB file in Microsoft Works and then export it to MDB file, in order the open a WDB file in MS Access.

## WDB file format
Microsoft Works Database is the native database format of the Microsoft Works office suite. Because of the proprietary nature of the format and some limitations. The WDB files can't be opened in any other software than Microsoft Works. In the file format a recurring, 10 byte header can be found before each of the ASCII text strings representing the values of the fields which were terminated by a NULL value. The header generally starts with a **\x0f** byte and NULL, followed by 4 data bytes alternated with NULLs.

### File structure

The structure of the WDB file is given below:
- **1st header**: from the beginning of the file, ending with \x25\x00\xf2 and 244 NULL bytes
- **2nd header**: beginning with \xffT - i.e. \xff\x54 and extending for 4096 bytes, that contains column/field names and other things, and seems to begin at byte position 6144.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. data byte 2 is the field number, data byte 3 is the record number (adding data byte 3, part 2 when it goes over 256 records).


## References ##

* [User:JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)
