{
  "date" : "2020-11-11",
  "keywords" : [ "BCP", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about BCP file format and APIs that can create and open BCP files.",
  "title" : "BCP - SQL Server Bulk Copy File Format",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is a BCP file?

BCP (Bulk Copy Format) is Microsoft SQL Server's technical data format that defines data structures to store different database data type values for import/export. The format fully defines the interpretation of each data column so that the set of values specified in the data file could be read. The [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) utility uses the BCP file format to read data from such a file and identify it.


## BCP File Format

The BCP format file is an XML document that defines the column order, name and data type. It lets users import/export large amount data from data file specifying these fields. This is helpful in bulk import of data values from data files. The number and order of data fields in the data file may be different than those in the destination table columns. This is when the BCP data format file comes to help by specifying the order and type of columns for importing the data.

The structure of the format file is represented in the following format.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP Data Types

|Data Type|Range|Representation|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) through 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Binary|1 through 8000 bytes|hexadecimal-encoded Unicode string format `Binary = 32000OCTET`|
|Bit|0 or 1|simple Unicode string Bit = "0" / "1"|
|Char|1 through 8000|Unicode String Format, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET with n = 4 x (2,147,483,647)|
|Date|0001-01-01 through 9999-12-31|YYYY-MM-DD string format|
|DateTime|1753-01-01 00:00:00.000 through 9999-12-31 23:59:59.997| Unicode YYYY-MM-DD hh:mm:ss[.nnn] string format|
|DateTime2|0001-01-01 00:00:00.0000000 through 9999-12-31 23:59:59.9999999.| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] string format|
|DateTimeOffset|0001-01-01 00:00:00.0000000 through 9999-12-31 23:59:59.9999999 in the Coordinated Universal Time (UTC) time zone| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] string format|
|Decimal|-1038 + 1 through 1038 – 1|Unicode string format `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1.79E+308 through -2.23E-308; 0; from 2.23E-308 through 1.79E+308|Unicode string format|
|Image|sequence of bytes that range from 0 through 231 – 1 (2,147,483,647)|hexadecimal-encoded Unicode string format|
|Int|-231 (-2,147,483,648) through 231 – 1 (2,147,483,647)|Unicode string format|

## References

 * [BCP Format - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)
