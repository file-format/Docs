{
  "date" : "2020-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "WOFF - Web Open File Format",
  "description":"A WOFF file is an open font format created in the Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-09-30"
}

## What is a WOFF file?

A file with .woff extension is a web font file based on the Web Open Font Format (WOFF). It has format-specific compressed container based on either TrueType (.TTF) or OpenType (.OTT) font types. WOFF was introduced with the aim to differ web fonts from fonts files used in desktop applications. In addition, the format targeted to reduce the latency of fonts transfer from server to client's computer over the network. Several tools are available that can convert WOFF files to TTF and other font file formats.

## WOFF File Format

WOFF font format compresses font data tables of table-based sfnt structures used in different font types such as TrueType, OpenType, and Open Font Format. It is like a container for these font types and also has the room to include font's metadata and private-use data to be included in the container. Converters use the sfnt files into a WOFF formatted file and user agents restore the encoded file for use with the web document. It is to be noted that the restored font data exactly matches the input font format from all aspects.

WOFF file Utilities often contain additional features such as glyph subsetting, validation or font feature additions but its not necessary. Both the creator and use agents must ensure that the validity of the underlying font data is preserved.

### WOFF File Structure

WOFF file structure is similar to that of sfnt fonts. It is based on a table directory that contains the lengths and offsets to each font data tables. All the tables are followed after this initial information. The file contains font database that are the same as in the original fonts. The order of the tables are also the same but each may be compressed. WOFF table directory replaces the original table directory though.

A WOFF file consists of following:

 * WOFFHeader	- File header with basic font type and version, along with offsets to metadata and private data blocks.
 * TableDirectory -	Directory of font tables, indicating the original size, compressed size and location of each table within the WOFF file.
 * FontTables -	The font data tables from the input sfnt font, compressed to reduce bandwidth requirements.
 * ExtendedMetadata	- An optional block of extended metadata, represented in XML format and compressed for storage in the WOFF file.
 * PrivateData- An optional block of private data for the font designer, foundry, or vendor to use.

### WOFF Header
The WOFF header comprises of an identifying signature which indicates the the kind of data included in the file. The WOFF header along with its fields is as follow.

|Type|Field Name|Description|
---|---|---|
|UInt32|signature	|0x774F4646 'wOFF' |
|UInt32|	flavor	|The "sfnt version" of the input font.|
|UInt32|	length	|Total size of the WOFF file.|
|UInt16|	numTables	|Number of entries in directory of font tables.|
|UInt16|	reserved	|Reserved; set to zero.|
|UInt32|	totalSfntSize	|Total size needed for the uncompressed font data, including the sfnt header, directory, and font tables (including padding).|
|UInt16|	majorVersion	|Major version of the WOFF file.|
|UInt16|	minorVersion	|Minor version of the WOFF file.|
|UInt32|	metaOffset	|Offset to metadata block, from beginning of WOFF file.|
|UInt32|	metaLength	|Length of compressed metadata block.|
|UInt32|	metaOrigLength	|Uncompressed size of metadata block.|
|UInt32|	privOffset	|Offset to private data block, from beginning of WOFF file.|
|UInt32|	privLength	|Length of private data block.|

## References

 * [w3 WOFF File Format](https://www.w3.org/TR/WOFF/)
