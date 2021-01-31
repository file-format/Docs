{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "POT - Microsoft PowerPOint Template File Format",
  "description":"Learn about POT file format and APIs that can create and open POT files.",
  "linktitle" : "POT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a POT file?

Files with .POT extension represent Microsoft PowerPoint template files created by PowerPoint 97-2003 versions. Files created with these versions of Microsoft PowerPoint are in binary format as compared to those created in Office OpenXML file formats using the higher versions of PowerPoint. The files, hence, generated can be used to create presentations that have same layout and other settings required to be applied to new files. These settings can include styles, backgrounds, colour palette, fonts and defaults. Such files are generated in order to create ready-to-use template files for official use.

## File Format Specifications ##

File format specifications for POT file format are not available individually by Microsoft. However, the template format is the same as that of the binary [PPT](/presentation/ppt/) file format and can be opened in MS PowerPoint for editing purpose. A POT file is identified by HEX identifier as follow:

```
D0 CF 11 E0 A1 B1 1A E1 00 00 00 00
```

 The MIME types associated with POT file format are:

* application/vnd.ms-powerpoint [official]
* application/mspowerpoint
* application/x-mspowerpoint
* application/powerpoint
* application/x-powerpoint
* application/x-dos_ms_powerpnt
* application/pot
* application/x-soffic

## References ##

* [PPT File Format specifications](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint File Formats](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)
