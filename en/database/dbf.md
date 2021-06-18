{
  "date" : "2021-06-15",
  "keywords" : [ "DBF", "extension", "dbf file", "dbf file format", "Database File Type", "Database File Format", "what is a dbf file", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DBF file format and APIs that can create and open DBF files.",
  "title" : "DBF -  dBase Database File",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-06-15"
}

## What is a DBF file?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. The DBF file type was introduced with dBASE II in 1983. It arranges multiple data records with Array type fields. The **xBase** database software which is pupular beacuse of its compatibility with a wide range of file formats; also supports the DBF files.

## DBF File Format
The DBF file format belongs to the dBASE database management system but it may be compatible with xBase or other DBMS softwares. The initial version of dbf file consisted of a simple table that could have data added, modified, deleted, or printed using the ASCII characters set. With the passage of time .dbf was improved, and additional files were added to increase the features and capabilities of the database system.

In modern dBASE a DBF file consists of a header, the data records, and the EOF (End of File) marker

- The header contains information about the file, such as the number of records and the number of types of fields used in the records.
- The records contain the actual data.
- The end of the file is marked by a single byte, with value 0x1A.

### File header
Layout of file header in dBase is given in following table:

| Byte | Contents | Meaning |
---|---|---|
| 0 | 1 byte | Valid dBASE for DOS file; bits 0–2 indicate version number, bit 3 indicates the presence of a dBASE for DOS memo file, bits 4–6 indicate the presence of a SQL table, bit 7 indicates the presence of any memo file (either dBASE m PLUS or dBASE for DOS) |
| 1–3 | 3 bytes | Date of last update; formatted as YYMMDD |
| 4–7 | 32-bit number | Number of records in the database file |
| 8–9 | 16-bit number | Number of bytes in the header |
| 10–11 | 16-bit number | Number of bytes in the record |
| 12–13 | 2 bytes | Reserved; fill with 0 |
| 14 | 1 byte | Flag indicating incomplete transaction[note 1] |
| 15 | 1 byte | Encryption flag[note 2] |
| 16–27 | 12 bytes | Reserved for dBASE for DOS in a multi-user environment |
| 28 | 1 byte | Production .mdx file flag; 1 if there is a production .mdx file, 0 if not |
| 29 | 1 byte | Language driver ID |
| 30–31 | 2 bytes | Reserved; fill with 0 |
| 32–n [note 3][note 4] | 32 bytes each | array of field descriptors (see below for layout of descriptors) |
| n + 1 | 1 byte | 0x0D as the field descriptor array terminator |

- The ISMARKEDO function checks this flag (BEGIN TRANSACTION sets it to 1, END TRANSACTION and ROLLBACK reset it to 0).
- If this flag is set to 1, the message Database encrypted appears.
- The maximum number of fields is 255.
- n means the last byte in the field descriptor array.

### Field descriptor array
Layout of field descriptors in dBASE:

| Byte | Contents | Meaning |
---|---|---|
| 0–10 | 11 bytes | Field name in ASCII (zero-filled) |
| 11 | 1 byte | Field type. Allowed values: C, D, F, L, M, or N (see next table for meanings) |
| 12–15 | 4 bytes | Reserved |
| 16 | 1 byte | Field length in binary (maximum 254 (0xFE)). |
| 17 | 1 byte | Field decimal count in binary |
| 18–19 | 2 bytes | Work area ID |
| 20 | 1 byte | Example |
| 21–30 | 10 bytes | Reserved |
| 31 | 1 byte | Production MDX field flag; 1 if field has an index tag in the production MDX file, 0 if not |

### Database records
Each record starts with a deletion (1-byte) flag. Fields are wrapped into records without field separators. All field data is ASCII. Depending on the field's type, the application imposes further restrictions. Here are field types in dBase:

| Field type | Mnemonic | What it accepts |
-------|-----|----|
| C | Character | Any ASCII text (padded with spaces up to the field's length) |
| D | Date | Numbers and a character to separate month, day, and year (stored internally as 8 digits in YYYYMMDD format) |
| F | Floating point | -, ., 0–9 (right justified, padded with whitespaces) |
| L | Logical | Y, y, N, n, T, t, F, f, or ? (when uninitialized) |
| M | Memo | Any ASCII text (stored internally as 10 digits representing a .dbt block number, right justified, padded with whitespaces) |
| N | Numeric | -, ., 0–9 (right justified, padded with whitespaces) |









## References ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)
