{
  "date" : "2020-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CFF2 - Compact Font File Format version 2",
  "description":"Learn about CFF2 File Format and APIs to create and open CFF2 files.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-10-21"
}

## What is a CFF2 file?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. It can't be used as a stand-alone program and depends on data in other OpenType tables.

## CFF2 File Format

The [CFF2 file format specifications](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) contains details about internal data layout, data types, tables and other internal information about the file format. It can be referred for developer's reference. Some of the details about these are as follow.

### Data Layout

The binary data of CFF2 file format is logically organized as a number of separate data structures. The layout within the binary data is as shown in the following table.

|Entry	|Comments|
---|---|
|Header	|Fixed location|
|Top DICT|	Fixed location|
|Global Subr INDEX|	Fixed location|
|Variation |Store|
|FDSelect	|Present only if there is more than one Font DICT in the Font DICT INDEX.|
|Font DICT INDEX	||
|Array of Font DICT|	Included in Font DICT INDEX.|
|Private DICT|	One per Font DICT.|

Only the first three structures are based on fixed locations. Remaining are reached via offsets, and their ordering can be changed.

### Data Types

The CFF2 file format uses the following data types.

|Name	|Range	|Description|
---|---|---|
|uint8	|0 to 255	|8-bit unsigned number|
|uint16	|0 to 65535|	16-bit unsigned number|
|uint32	|0 to 4294967295|	32-bit unsigned number|
|Offset	|varies|	1, 2, 3, or 4 byte offsets (specified by OffSize field in an Index table)|
|OffSize	|1 to 4|	1-byte unsigned number specifies the size of an Offset field or fields|

It stores all the multi-byte numeric data and offset fields in big-endian byte order. CFF2 format is free from padding bytes as it doesn't honour any alignment restrictions.

### DICT Data

CFF2 files contain the font dictionary data as key-value pairs in a compact tokenized format. Dictionary keys are encoded as 1 or 2 byte operators and dictionary values are encoded as variable-size numeric operands. There are three structures that use the DICT Data format: `Top DICT`, `Font DICT` and `Private DICT`. A number of integer operand types of varying sizes are defined and are encoded as shown in the following table (first byte of operand is b0, second is b1, and so on).

|Size	|b0 range	|Value range	|Value calculation|
---|---|---|---|
|1	|32 to 246|	-107 to +107	|b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3	|28|	-32768 to +32767|	b1 << 8 | b2|
|5	|29|	-(2^31) to +(2^31 - 1)|	b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Header

The binary data begins with a header having the format shown in Table below.

|Type	|Name	|Description|
---|---|---|
|uint8|	majorVersion|	Format major version. Set to 2.|
|uint8|	minorVersion|	Format minor version. Set to zero.|
|uint8|	headerSize|	Header size (bytes).|
|uint16|	topDictLength|	Length of Top DICT structure in bytes.|

## References

 * [CFF File Format](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/font/pdfs/5176.CFF.pdf)
 * [CFF2 File Format](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)
 * [Adobe Technical Note - Type2 Charstring Format](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/font/pdfs/5177.Type2.pdf)
