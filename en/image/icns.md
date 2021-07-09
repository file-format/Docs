{
  "date" : "2021-06-29",
  "keywords" : [ "ICNS", "extension", "file", "format", "image", "Apple Icon Image", "macOS", "Apple", "Icon" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ICNS - Apple Icon Image",
  "description":"Learn about ICNS file format and APIs that can create and open ICNS files.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-06-29"
}

## What is an ICNS file? ##

An icon format used by macOS programs is called an ICNS file. It allows 1-bit and 8-bit alpha bands and saves one or more pictures, usually made from [PNG](/image/png) documents. The program icon in the macOS browser and interface is displayed using ICNS files.

Based on the location, the same style icon can have multiple settings. The ICNS format has undergone numerous alterations and has evolved to the point where it may now be used as the foundation for various compatible formats. Here are some other important points you need to know:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource, and Mac OS icons Resource are some of the other names. 
* For icon information, a source in the resource branch is used.
* In most cases, a file contains numerous images. 1612 pixels square and 1024, 512, 256, 128, 48, 32, and 16 pixels square are supported picture sizes.


## ICNS File Format ##

The ICNS data format is a capsule for one or more images, supporting 1-bit bands and numerous image states. 
The operating system can resize icon pictures to fit the required display size. The larger icon pictures are typically saved as [JPEG](/image/jpeg/) 2000 or [PNG](/image/png) files. A type of both compressed and uncompressed ICNS files is possible. 

A header and binary icon data make up the structure of an ICNS file. The header contains 8 bytes of data, four of which are the magic literal and four of which are the file's length. The type and size of each icon picture are stored in the icon data section, which is followed by the binary image data. The picture size determines the binary section's size.

## Technichal Specification ##

### Header ###

|Offset|Size|Objective
---|---|---|
|0|4|Magic literal, must be "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Length of file, in bytes, msb first


### Icon data ###

|Offset|Size|Objective
---|---|---|
|0|4|Icon type
|4|4|Length of data, in bytes (including type and length), msb first
|8|Variable|Icon data

### Compression ###

The pixel data is compressed to some extent. The 32-bit ("is32", "il32", "ih32", "it32") and ARGB ("ic04", "ic05") pixels are often compressed (per channel) in a similar way to PackBits.

|Lead Value|Tail Bytes|Result (uncompressed)
---|---|---|
|0 - 127|1 - 128|1 - 128 Bytes
|128 - 255|1 Byte|3 - 130 Copies

## Reference ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)
