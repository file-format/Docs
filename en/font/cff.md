{
  "date" : "2020-08-20",
  "keywords" : [ "cff file", "cff file format", "what is a cff file", "file", "cff example", "cff file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CFF - Compact Font File Format",
  "description":"Learn about CFF File Format and APIs to create and open CFF files.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-10-21"
}

## What is a CFF file?

A file with .cff extension is a Compact Font Format and is also known as a PostScript Type 1, or CIDFont. CFF acts as a container to store multiple fonts together in a single unit known as a FontSet. The design of CFF fonts allow embedding PostScript language code that permits additional flexibility and extensibility of the format for usage with printer environments. CFF font files can be opened and converted using APIs such as [Aspose.Font](https://products.aspose.com/font).

## CFF File Format

CFF files are binary files that contain a structured data layout, has defined data types, a header, glyph organization and table dictionaries. More details about these can be found in the [compact font format specifications](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/font/pdfs/5176.CFF.pdf).

### Data Layout
The data layout of CFF file format is as shown below.

|Entry|Comments|
---|---|
|Header|–|
|NameINDEX|–|
|Top DICT INDEX|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Encodings–Charsets|–|
|FDSelect|CIDFonts only|
|CharStrings INDEX|per-font|
|Font DICT INDEX|per-font, CIDFonts only|
|Private DICT|per-font|
|Local Subr INDEX|per-font or per-Private DICT for CIDFonts|
|Copyright and Trademark Notices|–|

### Data Types

CFF data types are as shown in the following table.

|Name|Range|Description|
---|---|---|
|Card8|0 –255|1-byte unsigned number|
|Card16|0 – 65535|2-byte unsigned number|
|Offset|varies|1, 2, 3, or 4 byte offset (specified by OffSize field)|
|OffSize|1–4|1-byte unsigned number specifies the size of an Offset field or fields|
|SID|0 – 64999|2-byte string identifier|

### Header

The binary data begins with a header having the format shown in the following table.

|Type|Name|Description|
---|---|---|
|Card8|major|Format major version (starting at 1)|
|Card8|minor|Format minor version (starting at 0)|
|Card8|hdrSize| Header size (bytes)|
|OffSize|offSize|Absolute offset (0) size|


## References

 * [CFF File Format](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/font/pdfs/5176.CFF.pdf)
 * [Adobe Technical Note - Type2 Charstring Format](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/font/pdfs/5177.Type2.pdf)
