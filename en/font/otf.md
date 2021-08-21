{
  "date" : "2020-08-20",
  "keywords" : [ "otf file", "otf file format", "what is a otf file", "file", "otf example", "otf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OTF - TrueType Font File Format",
  "description":"Learn about OTF file format and APIs that can create and open OTF files.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-09-21"
}

## What is a OTF file?

A file with .otf extension refers to OpenType font format. OTF font format is more scalable and extends the existing features of [TTF](/font/ttf/) formats for digital typography. Developed by Microsoft and Adobe, OTF combines the features of PostScript and TrueType font formats. This makes OTF format to accommodate majority writing systems and that is why it is uniformly used on major computer platforms. The OpenType font format is supported by Mac OS X and Windows 2000 and later.

## Brief History

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. The modifications also included to introduce a more suitable font format that also meets the features of Adobe's Type 1 (PostScript) font formats.

Adobe, in 1996, joined Microsoft in its efforts to supersede both Apple's TrueType and its own Type 1 font formats. This resulted in combination of both underlying font formats to overcome the limitations and  add new extensions. This new technology was introduced the same year with the name **OpenType**.

## OTF File Format Specifications

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF Data Types
OTF files use the following data types which are all in Big Endian.

|Data Type|	Description|
---|---|
|uint8|	8-bit unsigned integer.|
|int8|	8-bit signed integer.|
|uint16|	16-bit unsigned integer.|
|int16|	16-bit signed integer.|
|uint24|	24-bit unsigned integer.|
|uint32|	32-bit unsigned integer.|
|int32|	32-bit signed integer.|
|Fixed|	32-bit signed fixed-point number (16.16)|
|FWORD|	int16 that describes a quantity in font design units.|
|UFWORD|	uint16 that describes a quantity in font design units.|
|F2DOT14|	16-bit signed fixed number with the low 14 bits of fraction (2.14).|
|LONGDATETIME|	Date and time represented in number of seconds since 12:00 midnight, January 1, 1904, UTC. The value is represented as a signed 64-bit integer.|
|Tag|	Array of four uint8s (length = 32 bits) used to identify a table, design-variation axis, script, language system, feature, or baseline|
|Offset16|	Short offset to a table, same as uint16, NULL offset = 0x0000|
|Offset32|	Long offset to a table, same as uint32, NULL offset = 0x00000000|
|Version16Dot16|	Packed 32-bit value with major and minor version numbers. (See Table Version Numbers.)|

### OTF Tables Directory

An OTF file starts with a table directory. This directory is the top-level collection of the tables in the font file. Depending on the number of fonts in a file, the table directory may be located at different location in the file. For example, in case the font file has only one font, the table directory starts at the byte 0 of the file. In case of multiple OpenType Fonts collection,
the table directory beginning is indicated in the TTCHeader.

|Type	|Name	|Description|
---|---|---|
|uint32	|sfntVersion|	0x00010000 or 0x4F54544F ('OTTO')|
|uint16|	numTables	|Number of tables.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, where “**” is an exponentiation operator).|
|uint16	|entrySelector	Log2 of the maximum power of 2 less than or equal to numTables (log2(searchRange/16), which is equal to floor(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - searchRange).|
|tableRecord|	tableRecords[numTables]	|Table records array—one for each top-level table in the font|


### Table Record

For each top-level table in the font, there is a Table Record which consists of the following fields.

|Type|	Name|	Description|
---|---|---|
|Tag|	tableTag|	Table identifier.|
|uint32|	checksum|	Checksum for this table.|
|Offset32|	offset|	Offset from beginning of font file.|
|uint32|	length	Length of this table.|

Each table in the OpenType font file is represented by names known as table tags. It is a must for all the records in the array to be sorted in ascending order by tag.

## References
 * [OpenType Font Specifications by Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType Overview](https://docs.microsoft.com/en-us/typography/truetype/)
