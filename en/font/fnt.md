{
  "date" : "2020-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FNT - Windows Font File",
  "description":"Learn about FNT file format and APIs that can create and open FNT files.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2020-10-30"
}

## What is a FNT file?

A file with .fnt extension is a font file that stores generic font information on Windows Operating systems. FNT files have been mostly replaced by TrueType (.TTF) and OpenType (.OTF) file formats, and is an obsolete font file format as of now. These files can store  a single rater or vector font. All device drivers support the Windows 2.x fonts. However, not all device drivers
support the Windows 3.0 version.

## FNT File Format

FNT files are capable of storing a single raster or vector font. The vector formats are more frequently used by GDI as compared to the raster where each charter's glyph is defined using a small bitmap. The obvious reason for the replacement of .fnt by .ttf and .otf is its raster format.

### Font File Header
The start of both raster and vector font files is common, followed by different information for each type of file. The font-file header includes for Windows 3.0 includes six new fields as follow which are set to zero to ensure compatibility with future versions of windows.

 * dFlags
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserved1

For detailed information about the headers for Windows 3.0 and 2.0, visit the [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## References
 * [Win32 Binaray Resource Formats](http://www.csn.ul.ie/~caolan/publink/winresdump/winresdump/doc/resfmt.txt)
 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [How to install or remove a font in Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)
