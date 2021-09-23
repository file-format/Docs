{
  "date" : "2021-02-25",
  "keywords" : [ "bdf file", "bdf file format", "what is a bdf file", "file", "bdf example", "bdf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BDF - Glyph Bitmap Distribution Format",
  "description":"Learn about BDF file format and APIs that can create and open BDF files.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2021-02-25"
}

## What is a BDF file?
BDF files are human readable form and usually distributed in an ASCII encoding. The file starts with global information relevant to the complete font, followed by the information and bitmaps for the individuals glyphs. The data in it shows for the font for a single size orientation. The metrics to use in more than one direction may be comprised in a single file. In BDF file, each item is contained on a separate line of text in the file. Spaces are used to separate the items on a line.

## BDF file format
The BDF shorts for Glyph Bitmap Distribution Format; owned by Adobe is a file format for saving fonts of bitmap type. The content takes the form of a text file intended to be computer as well as human readable. The BDF is particularly used in Unix X Window environments. It has been replaced widely by the PCF font format which is supposed to be more efficient, and by  OpenType and TrueType fonts.
### BDF file structure 
A BDF font file consists of three sections:

- a global section that applies to all glyphs in a font.
- a section with a separate entry for each glyph.
- the ENDFONT statement.

## Example
Here is an example font containing one glyph, for ASCII capital 'A'. Its global declarations start with the "STARTFONT" line and end with the "CHARS" line
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## References
 * [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glyph Bitmap Distribution Format (BDF) Specification](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)
