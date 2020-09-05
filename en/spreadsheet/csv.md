{
  "date" : "2019-12-10",
  "keywords" : [ "CSV", "file", "extension", "file format", "Comma Separated Values", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about CSV file format and APIs that can create and open CSV files.",
  "title" : "What is a CSV file?",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

Files with CSV (Comma Separated Values) extension represent plain text files that contain records of data with comma separated values. Each line in a CSV file is a new record from the set of records contained in the file. Such files are generated when data transfer is intended from one storage system to another. Since all applications can recognize records separated by comma, import of such data files to database is done very conveniently. Almost all spreadsheet applications such as Microsoft Excel or OpenOffice Calc can import CSV without much effort. Data imported from such files is arranged in cells of a spreadsheet for representation to user.

## Brief History ##

Following are some quick facts about the origin and history of CSV file format.

* 1972 - IBM Fortran (level H extended) compiler supported them under OS/360

* 1978 - List-directed input/output was supported by FORTRAN 77 that used commas and spaces for delimiters

* 2005 - CSV was standardized with [RFC4180](https://tools.ietf.org/html/rfc4180) as a MIME Content Type.

* 2013 - RFC4180's deficiencies were handled by a W3C recommendation

* 2015 - W3C made the first drafts of recommendations for CSV-metadata standards, that began as recommendation in December 2015

## Conversion of CSV Files ##

CSV files can be converted to several different file formats using the applications that can open these files. For example, Microsoft Excel can import data from CSV file format and save it to XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML and [HTML](/web/html/) file formats. Similarly, other desktop as well as online services provide the capability to export CSV files to HTML, ODS and [RTF](/word-processing/rtf/).

## CSV File Format ##

CSV file format is known to be specified under [RFC4180](https://tools.ietf.org/html/rfc4180). It defines any file to be CSV compliant if:

* Each record is located on a separate line, delimited by a line break (CRLF).  For example:
  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* The last record in the file may or may not have an ending line break.  For example:
  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx
* There may be an optional header line appearing as the first line of the file with the same format as normal record lines.  This header will contain names corresponding to the fields in the file and should contain the same number of fields as the records in  the rest of the file (the presence or absence of the header line should be indicated via the optional "header" parameter of this MIME type).  For example:
  * field_name,field_name,field_name CRLF
  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* ﻿Within the header and each record, there may be one or more fields, separated by commas.  Each line should contain the same number of fields throughout the file.  Spaces are considered part  of a field and should not be ignored.  The last field in the record must not be followed by a comma.  For example:
  * aaa,bbb,ccc
* Each field may or may not be enclosed in double quotes (however some programs, such as Microsoft Excel, do not use double quotes at all).  If fields are not enclosed with double quotes, then double quotes may not appear inside the fields.  For example:\
  * "aaa","bbb","ccc" CRLF
  * zzz,yyy,xxx
* Fields containing line breaks (CRLF), double quotes, and commas should be enclosed in double-quotes.  For example:
  * "aaa","b CRLF
  * bb","ccc" CRLF
  * zzz,yyy,xxx
* If double-quotes are used to enclose fields, then a double-quote appearing inside a field must be escaped by preceding it with another double quote.  For example:
  * "aaa","b""bb","ccc"

However, in light of modern usage, the delimiter is not limited to comma only and can be semicolon, tab or spaces as well. Applications such as Microsoft Excel provide option to specify the delimiter character for importing records from a CSV file.

## References ##

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)
