{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WOFF2 File - Web Open Font Format 2.0 File",
  "description": "Learn about what is a WOFF2 file and APIs that can create and open WOFF2 file.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff2"
    }
  },
  "lastmod": "2023-01-10"
}

## What is a WOFF2 file?

WOFF2 is a font file format that is a more compressed version of the Web Open Font Format (WOFF). It was developed as a way to reduce the file size of web fonts, allowing them to load faster and use less bandwidth. WOFF2 uses a compression algorithm called Brotli to compress the font data, which can result in file sizes that are significantly smaller than equivalent [WOFF](/font/woff/) fonts. This format is supported by most modern web browsers including Chrome, Firefox, Safari, Opera and Edge (version 14 onwards).

## WOFF2 File Format - More Information

The internal file structure of a WOFF2 font file is composed of several different parts, including a header, metadata, a table directory, and the font data itself.

 1. The header contains information about the overall format of the file, including the version number and the number of tables that are present in the file.

 1. Metadata section contains information such as font name, copyright, and other font-related information.

 1. The table directory contains information about the different tables that make up the font, including their location in the file and their length.

 1. The font data itself is divided into several different tables, each of which contains specific information about the font, such as its characters and their corresponding glyphs. These tables may include:

 * The 'glyf' table contains the actual font outlines, including the shape and size of each character.
 * The 'head' table contains general information about the font, such as its version number, design size, and so on.
 * The 'hmtx' table contains information about the metrics of the font, including the widths and positions of the characters.
 * Each table is compressed and stored in WOFF2 file format after it completed the process of encoding.

The structure overall is designed to allow for fast parsing and decoding, so that web browsers can quickly and efficiently load and display the font on a website.

### WOFF2 Header
The WOFF header comprises of an identifying signature which indicates the the kind of data included in the file. The WOFF header along with its fields is as follow.

|Type|Field Name|Description|
---|---|---|
|UInt32|signature	|0x774F4632 'wOF2' |
|UInt32|	flavor	|The "sfnt version" of the input font.|
|UInt32|	length	|Total size of the WOFF file.|
|UInt16|	numTables	|Number of entries in directory of font tables.|
|UInt16|	reserved	|Reserved; set to zero.|
|UInt32|	totalSfntSize	|Total size needed for the uncompressed font data, including the sfnt header, directory, and font tables (including padding).|
|UInt32|	totalCompressedSize	Total length of the compressed data block.|
|UInt16|	majorVersion	|Major version of the WOFF file.|
|UInt16|	minorVersion	|Minor version of the WOFF file.|
|UInt32|	metaOffset	|Offset to metadata block, from beginning of WOFF file.|
|UInt32|	metaLength	|Length of compressed metadata block.|
|UInt32|	metaOrigLength	|Uncompressed size of metadata block.|
|UInt32|	privOffset	|Offset to private data block, from beginning of WOFF file.|
|UInt32|	privLength	|Length of private data block.|


## References
 * [w3 WOFF2 File Format](https://www.w3.org/TR/WOFF2/)
