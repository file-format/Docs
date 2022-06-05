{
  "date" : "2019-10-11",
  "keywords" : [ "wmf file", "wmf file format", "what is a wmf file", "file", "wmf example", "wmf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "WMF - Microsoft Windows Metafile Format",
  "description":"Learn about WMF file format and APIs that can create and open WMF files.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a WMF file?

Files with WMF extension represent Microsoft Windows Metafile (WMF) for storing vector as well as bitmap-format images data. To be more accurate, WMF belongs to the vector file format category of Graphics file formats that is device independent. Windows Graphical Device Interface (GDI) uses the functions stored in a WMF file to display an image on the screen. A more enhanced version of WMF, known as Enhanced Meta Files (EMF), was published later that makes the format more feature rich. Practically, WMF are similar to SVG.

## WMF File Format Specifications ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. The file format consists of a series of variable-length records that contain graphics drawing commands, object definitions and properties. Since WMF files are based on commands rendered to the GDI for drawing the image, it is also known as a digital recording of the image which can be played back to reproduce that image. The complete file format specifications of WMF are available online and should be referred for development of applications to work with WMF files. A WMF file is organized into a:

* WMF Header Record
* WMF Record (s)
* WMF End-of-File Record

### WMF Header Record ###

The **META_HEADER Record** contains information that defines the characteristics of the metafile, including:

* The type of the metafile
* The version of the metafile
* The size of the metafile
* The number of objects defined in the metafile
* The size of the largest single record in the metafile

### WMF Placeable Header Record ###

The **META_PLACEABLE Record** contains extended information concerning the image, including:

* A bounding rectangle
* Logical unit size, for scaling
* A checksum, for validation

### WMF Record ###

WMF records have a generic format, which is specified in specifications document. Every WMF record contains the following information:

* The record size
* The record function
* Parameters, if any, for the record function

## References ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)
