{
  "date" : "2019-10-11",
  "keywords" : [ "tga file", "tga file format", "what is a tga file", "file", "tga example", "tga file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TGA File Format - A TARGA Graphic Image File",
  "description":"Learn about TGA file format and APIs that can create and open TGA files.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a TGA file?

A file with .tga extension is a raster graphic format and was created by Truevision Inc. It was designed for the TARGA (Truevision Advanced Raster Adapter) boards and provided Highcolor/truecolor display support for IBM-compatible PCs. It supports 8, 16, 24 and 32 bits per pixel and 8-bit alpha channel. It also supports lossless RLE compression that can be applied to reduce the image size. Digital photos and textures use the TGA image format.

## Brief History

Formation of TGA file format came into being in 1984 by AT&T EPICenter (later extracted and formed as an independent entity known as Truevision) that was working on marketing of new technologies developed by AT&T for color frame buffers. EPICenter was already working on its first two cards, the VDA (Video Display Adapter) and ICB (image capture board) for which work on two file types, .vda and .icb, was already in process. These file formats were codified and less broad specific file format TGA was introduced. TGA was an extension to what was already in use, and provided information such as width, height, pixel depth, associated color map and image origin.

TGA's 2.0 version, published in 1989, incorporated several enhanced features such as:

 * Thumbnails
 * Alpha channel
 * Gamma Value
 * Textual Metadata

Prime contributors to TGA's 2.0 version include Truevision's Shawn Steiner, Kevin Fiedly and David Spoelstra.

## TGA TARGA File Format Specifications

A TGA file consists of 2 main parts:

 * Header
 * Colour Pixel information

All the values in a TGA file are in littl-endian as per the format specifications.

### TGA Header

A TGA file header consists of the following 5 fields.

|Field no.|Length	|Field name	|Description|
---|---|---|---|
|1|	1 byte	|ID length|	Length of the image ID field (0-255)|
|2|	1 byte	|Color map type|	Whether a color map is included (0 - indicates that no color-map data is included with this image. 1 - indicates that a color-map is included with this image.)|
|3|	1 byte	|Image type|	Compression and color types (0- No Image Data Included. 1- Uncompressed, Color mapped image, 2- Uncompressed, True Color Image, 9- Run-length encoded, Color mapped image, 11- Run-Length encoded, Black and white image)|
|4|	5 bytes	|Color map specification|	Describes the color map|
|5|	10 bytes	|Image specification|	Image dimensions and format|

### Image and Color Map Data

|Field no.	|Length	|Field	|Description|
---|---|---|---|
|6	|From image ID length field|	Image ID|	Optional field containing identifying information|
|7	|From color map specification field|	Color map data|	Look-up table containing color map data|
|8	|From image specification field|	Image data|	Stored according to the image descriptor|

### Developer Area (Optional)

TGA Version 2.0 provides support for additional enhancements/extras which many developers wanted to store more information. The information is optional so that if a TGA decoder is not able to interpret it, it will be ignored.

### Extension Area (Optional)

|Field no.|	Length|	Field	|Description|
---|---|---|---|
|10|	2 bytes	|Extension size	|Size in bytes of the extension area, always 495|
|11|	41 bytes|	Author name	|Name of the author. If not used, bytes should be set to NULL (\0) or spaces|
|12|	324 bytes|	Author comment|	A comment, organized as four lines, each consisting of 80 characters plus a NULL|
|13|	12 bytes|	Date/time stamp	|Date and time at which the image was created|
|14|	41 bytes|	Job ID||
|15|	6 bytes|	Job time|	Hours, minutes and seconds spent creating the file (for billing, etc.)|
|16|	41 bytes|	Software ID	|The application that created the file.|
|17|	3 bytes|	Software version||
|18|	4 bytes|	Key color||
|19|	4 bytes|	Pixel aspect ratio||
|20|	4 bytes|	Gamma value||
|21|	4 bytes|	Color correction offset	|Number of bytes from the beginning of the file to the color correction table if present|
|22|	4 bytes|	Postage stamp |	Number of bytes from the beginning of the file to the postage stamp image if present|
|23|	4 bytes|	Scan line offset|	Number of bytes from the beginning of the file to the scan lines table if present|
|24|	1 byte|	Attributes type|	Specifies the alpha channel|

### File Footer (Optional)

The last 26 bytes of the file represent the footer, which if present means its likely a TGA version 2 file.

|Field No.|	Length|	Field|	Description|
---|---|---|---|
|28|	4 bytes|	Extension offset|	Offset in bytes from the beginning of the file|
|29|	4 bytes|	Developer area offset|	Offset in bytes from the beginning of the file|
|30|	16 bytes|	Signature|	Contains "TRUEVISION-XFILE"|
|31|	1 byte|	|	Contains "."|
|32|	1 byte|	|	Contains NULL|


## References

 * [TGA 2.0 File Format Specifications](http://www.dca.fee.unicamp.br/~martino/disciplinas/ea978/tgaffs.pdf)
 * [TGA by Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)
