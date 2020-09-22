{
  "date" : "2020-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TTF - TrueType Font File Format",
  "description":"TrueType fonts (TTF)are based on digital font technology specifications initially designed by Apple, Inc. Both Apple and Microsoft used TTF on Mac and Windows Operating systems.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-09-21"
}

A file with .ttf extension represents font files based on the TrueType specifications font technology. It was initially designed and launched by Apple Computer, Inc for Mac OS and was later adopted by Microsoft for Windows OS. TrueType fonts provide highest quality display on computer screens and printers without any dependency on resolution. All modern applications using fonts are able to work with TTF files. TTF font files are freely available over the internet and can also be converted to other font file formats such as OTF and WOFF.

## Brief History

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. The design objective behind TTF fonts was efficiency in storage and processing, and extensibility. Based on this extensibility, existing fonts can be converted to TrueType format.

Microsoft first used the TrueType fonts in Windows 3.1 in April 1992 after Apple agreed to license TrueType to Microsoft. It improved the rasterization mechanism, and improved its efficiency and performance.

## True Type File Format Specifications

A TrueType font file is a binary file that consists of a sequence of concatenated tables. Each table is a sequence of words and has a name known as  `Tag`. Each tag is of uint32 data type and consists of four characters. The first table in the file is font directory that gives access to other tables in the font file. Font data is contained in other tables followed after the font directory table.  Since each table is accessible by its tag, the tables can appear in any order in the file.

The required tables and their tag names are shown in the following table.

|**Tag**|**Table**|
---|---|
|'cmap'|	character to glyph mapping|
|'glyf'|	glyph data|
|'head'|	font header|
|'hhea'|	horizontal header|
|'hmtx'|	horizontal metrics|
|'loca'|	index to location|
|'maxp'|	maximum profile|
|'name'|	naming|
|'post'|	PostScript|

### Data Types
TrueType fonts use the standard integer and additional data types as listed in the following table.

|**Data Type** | **Description** |
---|---|
|shortFrac|	16-bit signed fraction|
|Fixed|	16.16-bit signed fixed-point number|
|FWord|	16-bit signed integer that describes a quantity in FUnits, the smallest measurable distance in em space.|
|uFWord|	16-bit unsigned integer that describes a quantity in FUnits, the smallest measurable distance in em space.|
|F2Dot14|	16-bit signed fixed number with the low 14 bits representing fraction.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Font Directory

The first table in the TrueType font is the font directory that provides access to the information required for accessing data in other tables. It further consists of:

 * `Offset subtable` - keeps record of the tables in the font and provides offset information to access each table in the directory
 * `Table Directory` - Contains entries for each table in the font

#### Offset SubTable
The offset subtable is shown below.

|**Type**|**Name**|**Description**|
---|---|---|
|uint32|	scaler type|	A tag to indicate the OFA scaler to be used to rasterize this font; see the note on the scaler type below for more information.|
|uint16|	numTables|	number of tables|
|uint16|	searchRange|	(maximum power of 2 <= numTables)*16|
|uint16|	entrySelector|	log2(maximum power of 2 <= numTables)|
|uint16|	rangeShift|	numTables*16-searchRange|

#### Table directory
The table directory comes right after the offset subtable. Its structure is as shown in the following table.

|**Type**|**Name**|**Description**|
---|---|---|
|uint32|	tag|	4-byte identifier|
|uint32|	checkSum|	checksum for this table|
|uint32|	offset|	offset from beginning of sfnt|
|uint32|	length|	length of this table in byte (actual length not padded length)|

Each table in a font file must have its own table directory entry. Entries in a table must be sorted in ascending order by tag.


## References
 * [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType Overview](https://docs.microsoft.com/en-us/typography/truetype/)
