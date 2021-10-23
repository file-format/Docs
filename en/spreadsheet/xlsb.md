{
  "date" : "2019-12-10",
  "keywords" : [ "XLSB", "file", "extension", "file format", "Excel Binary Spreadsheet File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an XLSB file and APIs that can create and open them.",
  "title" : "What is an XLSB file?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

## What is an XLSB file?

XLSB file format specifies the Excel Binary File Format, which is a collection of records and structures that specify Excel workbook content. The content can include unstructured or semi-structured tables of numbers, text, or both numbers and text, formulas, external data connections, charts and images. Unlike [XLSX](/spreadsheet/xlsx/) (which is based on Open XML file format), the XLSB represents binary Excel workbook file. XLSB files can be read and written to faster which makes them useful for working with large files. XLSB is seldom used to store workbooks as XLSX (and previously [XLS](/spreadsheet/xls/)) are the most common user selected file formats for saving workbooks. It can be opened by Microsoft Office 2007 and above.

## XLSB File Format Specifications ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Since then, the specifications have revised several times and the latest version of specifications (v 10.0) was published in April 2018. The specifications are available publicly by Microsoft as [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) and should be consulted by anyone for reading or writing files in XLSB file format.

## XLSB File Structure ##

An XLSB file is a package that consists of a collection of parts. These parts contain information about the contents of a workbook, including workbook data and the structure of the package. Some parts contain information stored using binary records, some as XML, while others contain information stored as a binary stream of bytes. Each binary record contains zero or more structured fields that contain the workbook data.

#### Package ####

An XLSB package is a [ZIP](/compression/zip/) archive that must contain exactly one workbook part. This part must be the target of a relationship in this package relationship part. The workbook part is the starting part in the XLSB document.

#### Part ####

A part is a stream of bytes that has an associated content type which specifies the nature and type of content stored in the part. Some parts store information in binary format while others store information as XML. The [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) section of specifications document lists the valid parts, content types and required/optional relationships among all parts in a package.

#### Relationship ####

A source and a target resource are connected by a relationship. A relationships can be:

**Package relationship:** where the target is a part and the source is the package as a whole

**Part-to-part relationship:** where the target is a part and the source is a part in the package

**Explicit relationship:** where a resource is referenced from the contents of a source part by referencing the ID attribute value of a relationship element

**implicit relationship** is a relationship that is not explicit

**Internal relationship:** where the target is a part in the package

**External relationship:** where the target is an external resource not in the package

#### Record ####

A record is the basic building block used to store information about features in a workbook. Each binary record is a variable-length sequence of bytes. A binary record consists of three components:

* a record type
* a record size, and
* the record data that is specific to that record type.

**Record Type:** The record type shows the type of record specified by the record. It also specifies the structure of record data specific to this record. The valid record types are listed in the [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) section of specifications document. The record type must be one or two bytes and must be greater than or equal to 128 and less than 16384.

**Record Size:** The record size specifies the count of bytes that specifies the total size of the record data. This value MUST be one to four bytes. This value MUST be one byte if the high bit in the low byte is equal to 0; otherwise, this value MUST be greater than one byte. If the count of bytes is greater than one byte, the high bit in each successive byte specifies whether an additional byte is used. If the high bit of the second byte is equal to 1, then this value MUST use an additional third byte. If the high bit of the third byte is equal to 1, then this value MUST use an additional fourth byte. The high bit of the fourth byte MUST be ignored. The value consists of the seven low bits of each byte combined. The low, least significant bits are contained within the first byte, and each successive byte contains higher order bits than the previous byte.

**Record Data:** The record data component contains fields that correspond to a particular record type and comprise the remainder of the record. The order and structure of the fields for a given record type listed in Record Enumeration are specified in the corresponding section for that record type in Records. The total size of the record data component MUST be equal to the record size. Fields in the record data component can contain simple values, arrays of values, structures of several fields, arrays of fields, and arrays of structures.

#### XLSB Record Example ####

The following record type and record size specify a **BrtCommentText** record with a size of 200 bytes:

11111101 00000100 11001000 00000001 [Record Fields]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, which equals 512. The record type value is 125 + 512, or 637, which corresponds to a **BrtCommentText** record type. The next byte is 11001000, specifying a low value of 72 and that the record size requires a second byte. The second byte is 00000001, specifying a higher value of 1 * 128 and that the record size does not require an additional byte. The record size is 72 + 128, or 200, which specifies the total size, in bytes, of the record data component. The fields in the record data component are specified by **BrtCommentText**.

## References ##

* [[MS-XLSB] - Excel (.xlsb) Binary File Format](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)
