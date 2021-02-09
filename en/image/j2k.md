{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "J2K",
  "description":"Learn about J2K file format and APIs that can create and open J2K files.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2020-08-03"
}

## What is a J2K file?

A **J2K** file is an image that is compressed using the wavelet compression instead of DCT compression. This file format is used by the Joint Photographic Experts Group (JPEG) 2000 files. J2K files store metadata information about the image file in XML unlike .jpeg or .jpg that use the EXIF format for this purpose. J2K files support 15-bit color, alpha transparency, and lossless compression. Several commercial APIs exist to decode JPEG 2000 imags such as J2K-Codec. A J2K file can be opened on Windows OS using the standard image viewers.

## J2K File Format ##

J2K file format is the same as that of JPEG 2000 which is often saved as .jp2 and .jpc. This makes J2K files follow the same approach of encoding metadata in XML format where the Standard 12234-1 is used as a reference between the Exif tags and the XML components. It is further improved by JPEG 2000 part-2 extension that combines the animation mechanism and code stream configurations into one single image. Such extended file-format files are saved as .jpx.

### Layout of a JPEG2000 File ###

JPEG2000 supports a variety of applications based on the conformance for extensible file formats. Though the simplest type can contain a single image, more complex types can include a series of images, stacked on top of each other or are time-based sequenced.

#### JP2 Box ####
It is the top-level building block of the JP2 file format and contains a type and length fields in the header, and a data secton. The most notable type of box is the contiguous codestream box. This box stores in its data section the JPEG2000 codestream.

#### JPEG2000 CodeStream ####

The JPEG2000 CodeStream is a sequence of bytes that is required to decode the JPEG2000 compressed image. In case the file doesn't have anything else other than this codestream, it is called a raw codestream file. Usually a JPEG codestream is the application of JPEG2000 compression algorithm on an image, though it is not the only way.

#### Tile Parts ####

A JPEG2000 encoded image is a collection of data units called packets. These packets are maintained in the codestream inside packet groups called tile-parts. Before encoding an image, the encoder devides the image into a rectangular grid of blocks, called tiles where each tile is encoded separately irrespective of other tiles.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 File Format" >}}

## J2K Compression ##
JPEG 2000 uses wavelet compression technology making it fast based on the fact that relatively few pixels are shown in whatever viewport or window the viewer displays the image. This can be emphasized by the fact that only a few megabytes of pixels will appear on the screen for very large size images (in gigabytes). This helps to rapidly fetch and render only that part of the image data which is required to populate the display pixels. This also requires high-speed decompression technology to speed up the image fetching mechanism for creating the imagery required on the fly.

J2K takes advantage of fast decompression and fetches only necessary information for pixel data to render part of visible images quickly to the screens. J2K is designed primarily for the viewing of data and not editing it.

## J2K Identification ##
JPEG 2000 files have signature bytes 6A 50 20 20.

### Mime Types ###
Registered Mime Types for JPEG 2000 files include:
  * image/jp2
  * image/jpx
  * image/jpm
  * video/mj2

## Improvements over the JPEG standard ##
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
