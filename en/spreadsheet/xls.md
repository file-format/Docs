{
  "date" : "2019-12-16",
  "keywords" : [ "XLS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an XLS file and APIs that can create and open them.",
  "title" : "What is XLS file format? Learn from File Format Experts!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-16"
}

## What is an XLS file?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Brief History

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* Version 8 (released with office 97): VBA was introduced as a standard language and removed natural language labels were incorporated in this version for the first time. It also introduced a paper clip office assistant for the first time.
* Version 9 (Released with office 2000): There were only minor changes in Version 9 where paper clip office assistant could simultaneously hold multiple objects that were not previously possible.
* Version 10 (Released with office XP): This version did not contain any noticeable improvement.
* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS File Format Specifications ##

Data is arranged in an XLS file as binary streams in the form of a compound file as described in [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx) document by Microsoft.

#### Stream and Substream ####

A workbook is represented by the workbook stream. Each worksheet in a workbook is represented by Substreams. In addition, it has Chart Sheet Substream, Macro Sheet Substream, or Dialog Sheet Substream that follows the Global Substream. Each binary stream or substream that contains workbook data MUST be written as a series of binary records.

#### Record ####

Information about features in a workbook is stored as a record that is a variable-length sequence of bytes. A binary record consists of the following three components:

**Record Type:**  The record type is a two-byte unsigned integer that specifies what type of information is specified by the record and how the structure of the record data specific to this record is ordered and structured. Record type values MUST be a value from the Record Enumeration (section 2.3) or the record MUST make use of the future record architecture (section 2.1.6).

**Record Size**: The record size is a two-byte unsigned integer that specifies the count of bytes that specifies the total size of the record data. The record size MUST be greater than or equal to 0 and MUST be less than or equal to 8224.

**Record Data:** The record data component contains fields that correspond to a particular record type and comprise the remainder of the record. The order and structure of the fields for a given record type are specified in the corresponding section for that record type. The size of the record data component MUST be equal to the record size. Fields in the record data component can contain simple values, arrays of values, structures of several fields, arrays of fields, and arrays of structures.

#### Cell Table ####

Cells are the fundamental blocks of a workbook that store the workbook contents like text, formulas and numerical data. Cells maintain the record of the stored data via a data structure called the Cell Table. The Cell Table itself is stored in the sequence of records that conform to the CELLTABLE rules defined in the specifications document. It consists of a series of row blocks where the rows are arranged in row blocks. Each row block contains rows from the first row containing data to the last row containing data.

Data or row formatting is saved in a Row record for each row block. Every cell that contains data or individual cell formatting is represented by a record. Formatting associated with a cell can be derived from individual cell formatting, row formatting, column formatting, or the default cell format. The order of precedence for formatting is individual cell formatting with the highest precedence, followed by row formatting, and then column formatting, and then the default cell format. Cells that do not contain data and do not contain individual formatting are not saved.

#### Formulas ####

A formula is a sequence of values, cell references, names, functions, or operators in a cell that together produce a new value. Formulas are stored in a tokenized representation known as "parsed expressions." A parsed expression is converted into a textual formula at runtime for display and user editing. Cell formulas are specified by the Formula record. Array formulas are specified by the Array record. Shared formulas are specified by the ShrFmla record.

#### Charts ####

The chart sheet specifies a chart, a graphic that displays data or the relationships between sets of data in a visual form, and a chart data cache, a local copy of the data that is used in the chart data is missing or if links to external data sources are broken. The chart specifies one or two-axis groups, a set of axes the chart data is plotted against, and the set of series, trendlines, and error bar specified in the chart. Each axis group specifies one to four chart groups that specify the type of visualization used to display the data. Each series, trendline, and error bar specifies a chart group it is associated with.

#### Metadata ####

Metadata is additional data associated with a particular cell or its content. Metadata is recorded in BIFF8 for future extensibility purposes only.

#### Pivot Tables ####

A PivotTable is a mechanism for summarizing source data to get an overview of the distribution of that data. In a PivotTable, applicable columns of the source data become fields that can be used to summarize data. When the source data of the PivotTable is OLAP source data, OLAP hierarchies and some other OLAP entities become fields in the PivotTable.
A PivotTable has two major parts, a PivotCache and a PivotTable view. There can be multiple PivotTable views based on a single non-OLAP PivotCache.

#### Styles ####

This overview describes how formatting and protection information for cells in a sheet (1) is specified. Cell formatting is composed of several sets of properties:

* Font properties (bold, italic, font color, font size, etc…)
* Fill properties (foreground color, background color, pattern, gradient, etc…)
* Alignment properties (left, center, right alignment, etc…)
* Border properties (left, right, top, bottom, thick or thin, color, etc…)
* Number formatting properties (date, time, number of decimal places, etc…)
* Protection properties (locked, hidden, etc…)

These properties, as a whole, describe how a particular cell is displayed and printed.

## References ##

* [[MS-XLS] - Excel Binary File Format Structure](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Compound File Binary File Format](https://msdn.microsoft.com/en-us/library/dd942138.aspx)
