{
  "date": "2021-02-25",
  "keywords": [
    "ttc file",
    "ttc file format",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "TTC - TrueType Collection File Format",
  "description": "A TrueType Collection (TTC) file combines multiple fonts into a single file. Both Apple and Microsoft used TTF on Mac and Windows Operating systems.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ttc"
    }
  },
  "lastmod": "2021-02-25"
}

## What is a TTC file?
The TTC is abbreviated as TrueType Collection is an extension of True Type format. A TTC file can combine the multiple font files into it. These files are beneficial for combining multiple fonts that share many glyphs in common. Before Windows 2000, the TTC files were used in Chinese, Japanese, and Korean versions of windows but later on the support were available for all regions.  


## The Structure of Font Collection File 
A TTC file consists of a TTC Header table, Table Directories, and multiple OpenType tables. The TTC Header must be found at the start of the file. A complete table directory for each font must be existed. The TableDirectory format should be similar as existed in a non-collection file. The table counts in all directories within a TTC file are calculated from the start of a TTC file.
The tables in a TTC file are referenced through the table directory of their respective fonts. A few of the OpenType tables must appear multiple times, once for each font added in the TTC. Whereas the other tables may be shared by multiple fonts in the TTC file.

### TTC Header
Two versions of the TTC Header table are available so far: 
- Version 1.0 is used for TTC files without digital signatures. 
- Version 2.0 can be used for TTC files with or without digital signatures.
Here are the TTC Header tables of both versions:

**TTC Header Version 1.0:**

|Type|Name|Description|
---|---|---|
|TAG|ttcTag|Font Collection ID string: 'ttcf' (used for fonts with CFF or CFF2 outlines as well as TrueType outlines)|
|uint16|majorVersion|Major version of the TTC Header, = 1.|
|uint16|minorVersion|Minor version of the TTC Header, = 0.|
|uint32|numFonts|Number of fonts in TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array of offsets to the TableDirectory for each font from the beginning of the file|

**TTC Header Version 2.0:**

|Type|Name|Description|
---|---|---|
|TAG|ttcTag	|Font Collection ID string: 'ttcf'|
|uint16|	majorVersion	|Major version of the TTC Header, = 2.|
|uint16|	minorVersion	|Minor version of the TTC Header, = 0.|
|uint32|	numFonts	|Number of fonts in TTC|
|Offset32|	tableDirectoryOffsets[numFonts]	|Array of offsets to the TableDirectory for each font from the beginning of the file|
|uint32|	dsigTag	|Tag indicating that a DSIG table exists, 0x44534947 ('DSIG') (null if no signature)|
|uint32|	dsigLength	|The length (in bytes) of the DSIG table (null if no signature)|
|uint32|	dsigOffset	|The offset (in bytes) of the DSIG table from the beginning of the TTC file (null if no signature)|

## References
 * [The OpenType Font File](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)
