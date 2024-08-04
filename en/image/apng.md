{
  "date": "2019-10-11",
  "keywords": [
    "apng file",
    "apng file format",
    "what is a apng file",
    "file",
    "apng example",
    "apng file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "APNG File Format - Animated Portable Network Graphic File",
  "description": "Learn about APNG file format and APIs that can create and open APNG files.",
  "linktitle": "APNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-apng"
    }
  },
  "lastmod": "2020-09-10"
}

## What is a APNG file?

A file with .apng (Animated Portable Network Graphics) extension is a raster graphic format and is an unofficial extension to the Portable Network Graphic ([PNG](/image/png/) ). It comprises of multiple frames (each of PNG image) that represents an animation sequence. This gives similar visualization as a [GIF](/image/gif/) file. APNG files support 24-bit images and 8-bit transparency. APNG is backward compatible with non-animated GIF files. APNG files use the same .png extension and can be opened by applications such as Mozilla Firefox, Chrome with APNG support, iMessage apps for iOS 10.

## Brief History

 * APNG specifications were created in 2004 to provide support for animated PNG Images
 * APNG decoders were developed with much smaller size and using the back of the PNG decoder
 * After continuous deliberations, a new MIME type image/apng was formulated while keeping the extension the same as .png instead of .apng
 * APNG was officially rejected by the PNG group on April 20, 2007 owing to its uniformity to PNG images while at the same time having different specifications

## APNG File Format

APNG files are stored as binary files on disc and use the extended specifications of PNG for animated images. The first frame of an APNG file is a normal PNG stream that is readable by PNG decoders for display. APNG file format follow the PNG specifications and data is stored in segments called chunks. However, APNG introduced the following new chunks:

`Animation Control Chunk (acTL)` - Indicates that this file is an animated PNG file rather than a normal PNG file. It acts as a marker and comes before the IDAT chunk. It also contains the number of frames and information about times to loop the animations

`Frame Control Chunk` - Occurs at start of each and metadata information such as dimensions, position, transparency application, and replacement information by previous or next frame once it is over.

`Frame Data Chunk` - Stores frame's contents and starts with a sequence number. This sequence number has the same structure as the default image's IDAT chunk.

{{< figure src="../APNG.png" alt="Animated PNG - APNG File Format" >}}

APNG is backward compatible with PNG as the lateral's specifications were designed in such a way that an application reading a PNG file is supposed to simply ignore the chunks which it does not understand. Specifications regarding bit depth, color type, compression, filters, interlace methods, and palette information are used the same as that of default PNG format. When you [take a screenshot on Mac](https://how-to-take-screenshot.com/mac/), it is saved as PNG file by default. 

## APNG vs GIF

With GIF already in place and being used over a long period of time, you may wonder how is APNG different than GIF. Following is a set of comparison between APNG and GIF that gives a brief idea of both file formats.

||APNG|GIF|
---|---|---|
|Published|2004|1987|
|Color Depth|24 bit|8 bit|
|Frame Rate|Unlimited|10 frames per second|
|Transparency|Complete and partial|Complete|
|Compression|Very Good|Good|

## References

 * [APNG File Format](https://en.wikipedia.org/wiki/APNG)
 * [Official PNG Format Specifications](https://www.w3.org/TR/PNG/)
