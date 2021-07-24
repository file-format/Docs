{
  "date" : "2019-10-11",
  "keywords" : [ "j2c file", "j2c file format", "what is a j2c file", "file", "j2c example", "j2c file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "J2C",
  "description":"Learn about J2C file format and APIs that can create and open J2C files.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-02-14"
}

## What is a J2C file?

A file with .j2c extension is a variant of JPEG file format and is compressed with the wavelet compression. It has nearly identical system of markers and segments to JPEG 2000 file format. The J2C file format is as defined in the Part 1 of the JPEG 2000 stand that supports both lossy and lossless compression. The JPEG 2000 codestream was designed to be embedded in [JP2](/image/jp2/) or another file format, although it may appear in a file by itself. A J2C file can be opened using Adobe Photoshop 2020, Adobe Illustrator 2020, and Corel Paintshop Pro.

## J2C File Format

J2C file format is the same as that of JPEG 2000 which is often saved as .jp2 and .jpc. This makes J2C files follow the same approach of encoding metadata in XML format where the Standard 12234-1 is used as a reference between the Exif tags and the XML components. It is further improved by JPEG 2000 part-2 extension that combines the animation mechanism and code stream configurations into one single image. Such extended file-format files are saved as [.jpx](/image/jpx/).

### Layout of a JPEG2000 File

JPEG2000 supports a variety of applications based on the conformance for extensible file formats. Though the simplest type can contain a single image, more complex types can include a series of images, stacked on top of each other or are time-based sequenced.

#### JP2 Box
It is the top-level building block of the JP2 file format and contains a type and length fields in the header, and a data secton. The most notable type of box is the contiguous codestream box. This box stores in its data section the JPEG2000 codestream.

#### JPEG2000 CodeStream

The JPEG2000 CodeStream is a sequence of bytes that is required to decode the JPEG2000 compressed image. In case the file doesn't have anything else other than this codestream, it is called a raw codestream file. Usually a JPEG codestream is the application of JPEG2000 compression algorithm on an image, though it is not the only way.

#### Tile Parts ####

A JPEG2000 encoded image is a collection of data units called packets. These packets are maintained in the codestream inside packet groups called tile-parts. Before encoding an image, the encoder devides the image into a rectangular grid of blocks, called tiles where each tile is encoded separately irrespective of other tiles.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 File Format" >}}

## J2C Compression
JPEG 2000 uses wavelet compression technology making it fast based on the fact that relatively few pixels are shown in whatever viewport or window the viewer displays the image. This can be emphasized by the fact that only a few megabytes of pixels will appear on the screen for very large size images (in gigabytes). This helps to rapidly fetch and render only that part of the image data which is required to populate the display pixels. This also requires high-speed decompression technology to speed up the image fetching mechanism for creating the imagery required on the fly.

J2C takes advantage of fast decompression and fetches only necessary information for pixel data to render part of visible images quickly to the screens. J2C is designed primarily for the viewing of data and not editing it.

## J2C Identification
JPEG 2000 files have signature bytes `FF 4F FF 51`.

### Mime Types
Registered Mime Types for JPEG 2000 files include:
  * image/j2c
  * image/jpx
  * image/jpm
  * video/mj2

## Improvements over the JPEG standard
Improvements over the JPEG standard include:
  * Superior compression performance
  * Multiple resolution representation
  * Progressive transmission by pixel and resolution accuracy
  * Choice of lossless or lossy compression
  * Error resilience, Flexible file format
  * High dynamic range support
  * Side channel spatial information

## References ##
  * [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)
