{
  "date": "2019-10-11",
  "keywords": [
    "png file",
    "png file format",
    "what is a png file",
    "file",
    "png example",
    "png file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PNG File Format - Raster Image File",
  "description": "Learn about PNG file format and APIs that can create and open PNG files.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-png"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a PNG file?

A **PNG** (Portable Network Graphics) file is a raster image file format that uses lossless compression. This file format was created as a replacement of Graphics Interchange Format ([GIF](/image/gif/)) and has no copyright limitations. However, PNG file format does not support animations. PNG file format supports lossless image compression that makes it popular among its users. With the passage of time, PNG has evolved as one of the widely used image file formats.

## Brief History of PNG File Format

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Key events with respect to PNG file formats are listed below:

* October 1996: PNG specifications Version 1.0 were released and later appeared as [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. The same became a W3C Recommendation in October 1996.
* December 1998: Version 1.1, with some small changes and the addition of three new chunks, was released.
* August 1999: Version 1.2, adding one extra chunk, was released.
* November 2003: PNG became an International Standard (ISO/IEC 15948:2003). This version of PNG differs only slightly from version 1.2 and adds no new chunks.
* March 2004: ISO/IEC 15948:2004

PNG is popular file format now and it is used as default file format when you take screenshot on Mac and other operating systems.

## Functional Comparison of GIF and PNG

PNG file format was designed to be simple and portable, legally unencumbered, interchangeable, flexible and robust. The following table lists the GIF features that are inherited by PNG file format in addition to new features.

|Feature|GIF|PNG|
---|---|---|
|Index-color images of up to 256 colors|Yes|Yes|
|Support for streaming|Yes|Yes|
|Transparency|Yes|Yes|
|Ancillary information|Yes|Yes|
|Hardware and Platform Independence|Yes|Yes|
|Effective|Yes|Yes|
|Truecolor images of up to 48 bits per pixel|No|Yes|
|Grayscale images of up to 16 bits per pixel|No|Yes|
|Full alpha channel (general transparency masks)|No|Yes|
|Image gamma information|No|Yes|
|Reliability|No|Yes|
|Faster initial presentation|No|Yes|

## PNG File Structure

Almost all Operating Systems have support for opening PNG files. For example, Microsoft Windows viewer has the capability to open PNG files as the OS has by default the support available as part of installation. A PNG file consists of a PNG `signature` followed by a series of //chunks//.

### PNG File Header

The first eight bytes of a PNG file always contain the following (decimal) values:

{{{137 80 78 71 13 10 26 10 }}}

This signature indicates that the remainder of the file contains a single PNG image, consisting of a series of chunks beginning with an IHDR chunk and ending with an IEND chunk.

### Chunks ###

Each chunk consists of four parts:

**Length:** A 4-byte unsigned integer giving the number of bytes in the chunk's data field. The length counts only the data field, not itself, the chunk type code, or the CRC. Zero is a valid length. Although encoders and decoders should treat the length as unsigned, its value must not exceed 231 bytes.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Chunk Data:** The data bytes appropriate to the chunk type, if any. This field can be of zero length.

**CRC:** A 4-byte CRC (Cyclic Redundancy Check) calculated on the preceding bytes in the chunk, including the chunk type code and chunk data fields, but not including the length field. The CRC is always present, even for chunks containing no data.

The chunk data length can be any number of bytes up to the maximum; therefore, implementors cannot assume that chunks are aligned on any boundaries larger than bytes.

Chunks can appear in any order, subject to the restrictions placed on each chunk type. (One notable restriction is that IHDR must appear first and IEND must appear last; thus the IEND chunk serves as an end-of-file marker.) Multiple chunks of the same type can appear, but only if specifically permitted for that type.

#### Chunk Types

The Chunk Types are categorized into **Critical** and **Ancillary** chunks based on the 4-byte case-sensitive ASCII value assigned to the Chunk Type. All implementations must understand and successfully render the standard critical chunks. A valid PNG image must contain an IHDR chunk, one or more IDAT chunks, and an IEND chunk.

### Compression

PNG compression method 0 (the only compression method presently defined for PNG) specifies deflate/inflate compression with a sliding window of at most 32768 bytes. Deflate compression is an LZ77 derivative used in zip, gzip, pkzip, and related programs. Extensive research has been done supporting its patent-free status. The compressed data within the zlib datastream is stored as a series of blocks, each of which can represent raw (uncompressed) data, LZ77-compressed data encoded with fixed Huffman codes, or LZ77-compressed data encoded with custom Huffman codes. A marker bit in the final block identifies it as the last block, allowing the decoder to recognize the end of the compressed datastream.

#### Pre-Compression Filtering

Pre-compression filters are applied to prepare the image data for optimum compression. PNG filter method defines five basic filter types as follow:

|Filter Type|Name|Predicted Value|
---|---|---|
|0|None|The scanline is transmitted unmodified|
|1|Sub|Transmits the difference between each byte and the value of the corresponding byte of the prior pixel.|
|2|Up|The Up() filter is just like the Sub() filter except that the pixel immediately above the current pixel, rather than just to its left, is used as the predictor.|
|3|Average|The Average() filter uses the average of the two neighbouring pixels (left and above) to predict the value of a pixel.|
|4|Paeth|The Paeth() filter computes a simple linear function of the three neighbouring pixels (left, above, upper left), then chooses as predictor the neighbouring pixel closest to the computed value.|

Filtering algorithms are applied to `bytes`, not to pixels, regardless of the bit depth or color type of the image. The filtering algorithms work on the byte sequence formed by a scanline. If the image includes an alpha channel, the alpha data is filtered in the same way as the image data.

When the image is interlaced, each pass of the interlace pattern is treated as an independent image for filtering purposes. The filters work on the byte sequences formed by the pixels actually transmitted during a pass, and the "previous scanline" is the one previously transmitted in the same pass, not the one adjacent in the complete image. Note that the subimage transmitted in any one pass is always rectangular, but is of smaller width and/or height than the complete image. Filtering is not applied when this subimage is empty.

## References ##

* [PNG - Home Page](http://www.libpng.org/pub/png/)
* [Take Screenshot on Mac](https://how-to-take-screenshot.com/mac/)