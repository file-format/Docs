{
  "date" : "2020-08-20",
  "keywords" : [ "fon file", "fon file format", "what is a fon file", "file", "fon example", "fon file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FON - Font Library File",
  "description":"Learn about FON file format and APIs that can create and open FON files.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-10-30"
}

## What is a FON file?

A file with .fon extension is a Microsoft Windows 3.x font library that is actually an executable file but renamed to .fon. It is a collection of [.fnt](/font/fnt/) files in itself and applications reference it while accessing system font. That is why it acts as a resource file. It can be opened on Windows OS using Microsoft Windows Font View application.

## FON File Format

A FON file contains font resources and has Resource (.res) file format. The .res file format specifies the file header as well as data section specifications. A .fnt is also a resource data file that is included with a resource file. FON files have binary file format and have application/octet-stream MIME type.

Font resources, unlike other type of resources, are not added to the resources of an application. Instead they are added to the EXE files and renamed to .fon files, resulting in library files instead of applications. Multiple Individual fonts constitute components of a font group where each group follows a resource group structure. Font resources use these resource group structures. The group header has all the information that is required to access a specific font from the group. A font component resource has the following format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
A single .rc resource file can have mixed resource declarations. Font groups can be anywhere in the resource file and needs not to be contigous. It is must for programs creating .RES files to add manual entry of FONTDIR. Following is the structure of group header.

 ```
    [Normal resource header (type = 7)]

    WORD NumberOfFonts; // Total number in .RES file
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
  WORD   dfVersion;
  DWORD  dfSize;
  char   dfCopyright[60];
  WORD   dfType;
  WORD   dfPoints;
  WORD   dfVertRes;
  WORD   dfHorizRes;
  WORD   dfAscent;
  WORD   dfInternalLeading;
  WORD   dfExternalLeading;
  BYTE   dfItalic;
  BYTE   dfUnderline;
  BYTE   dfStrikeOut;
  WORD   dfWeight;
  BYTE   dfCharSet;
  WORD   dfPixWidth;
  WORD   dfPixHeight;
  BYTE   dfPitchAndFamily;
  WORD   dfAvgWidth;
  WORD   dfMaxWidth;
  BYTE   dfFirstChar;
  BYTE   dfLastChar;
  BYTE   dfDefaultChar;
  BYTE   dfBreakChar;
  WORD   dfWidthBytes;
  DWORD  dfDevice;
  DWORD  dfFace;
  DWORD  dfReserved;
  char   szDeviceName[];
  char   szFaceName[];
  };
```

## References
 * [Win32 Binaray Resource Formats](http://www.csn.ul.ie/~caolan/publink/winresdump/winresdump/doc/resfmt.txt)
 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
