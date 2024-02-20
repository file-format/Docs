{
  "date": "2019-10-11",
  "keywords": [
    "tiff file",
    "tiff file format",
    "what is a tiff file",
    "file",
    "tiff example",
    "tiff file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "TIFF - Image File Format",
  "description": "Learn about TIFF file format and APIs that can create and open TIFF files.",
  "linktitle": "TIFF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tiff"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a TIFF file?

TIFF or TIF, Tagged Image File Format, represents raster images that are meant for usage on a variety of devices that comply with this file format standard. It is capable of describing bilevel, grayscale, palette-color and full-color image data in several color spaces. It supports lossy as well as lossless compression schemes to choose between space and time for applications using the format. The format is not machine dependent and is free from bounds like processor, operating system, or file systems.

## Brief History of TIFF File Format

TIFF file format was initially created by Aldus Corporation in the fall of 1986, after a series of meetings with various scanner manufacturers and software developers. The primary purpose of TIFF file format was to provide a common scanned image file format for all the desktop scanner vendors. Starting with support for only binary image format, the format evolved to the support of grayscale and color images with the passage of time. The initial version of TIFF file format specifications can be labeled as Reivision 3.0 as there were two earlier draft releases. A major Revision 5.0 was published in 1988 that added support for palette color images and LZW compression. Revision 6.0 of TIFF file formats were published in 1992 after that. In 1994, Adobe Systems acquired Aldus and the specifications are now available and maintained by Adobe Systems.

## TIFF File Format Specifications

TIFF file format is extensible and has underwent several revisions that allows the inclusion of an unlimited amount of private or special-purpose information. A TIFF file begins with an 8-byte header where the bytes are number from 0 to N. The largest possible TIFF file is 2**32 bytes in length. The file begins with an 8-byte image file header that points to an image file directly (IFD). An IFD contains information about the image as well as pointers to the actual image data.

### TIFF File Header

The 8-byte TIFF file header contains the following information:

**Bytes 0-1:**  The byte order used within the file. Legal values are:“II”(4949.H)“MM”  (4D4D.H).

In the “II” format, byte order is always from the least significant byte to the most significant byte, for both 16-bit and 32-bit integers This is called little-endian byte order. In the “MM” format, byte order is always from most significant to least significant, for both 16-bit and 32-bit integers. This is called big-endian byte order.

**Bytes 2-3:**    An arbitrary but carefully chosen number (42) that further identifies the file as a TIFF file.The byte order depends on the value of Bytes 0-1.

**Bytes 4-7:**    The offset (in bytes) of the first IFD. The directory may be at any location in the file after the header but must begin on a word boundary. In particular, an Image File Directory may follow the image data it describes. Readers must follow the pointers wherever they may lead.The term byte offset is always used in this document to refer to a location with respect to the beginning of the TIFF file. The first byte of the file has an offset of 0.

### Image File Directory

An IFD contains information about the image as well as pointers to the actual image data.. It consists of a 2-byte count of the number of directory entries (i.e. the number of fields), followed by a sequence of 12-byte field entries, followed by a 4-byte offset of the next IFD (or 0 if none). There must be at least 1 IFD in a TIFF file and each IFD must have at least one entry.

#### IFD Entry

Each 12-byte IFD Entry is in the following format.


|Bytes|Description
---|---|
|0-1|The Tag that identifies the field
|2-3|The field type
|4-7|Count of the indicated type
|8-11|The Value Offset, the file offset (in bytes) of the Value for the field.The Value is expected to begin on a word boundary; the correspond-ing Value Offset will thus be an even number. This file offset may point anywhere in the file, even after the image data

A TIFF field is a logical entity consisting of TIFF tag and its value. This logical concept is implemented as an IFD Entry, plus the actual value if it doesn’t fit into the value/offset part, the last 4 bytes of the IFD Entry. The terms TIFF field and IFD entry are interchangeable in most contexts.

### Baseline TIFF ###

Baseline TIFF is the core of TIFF, the essentials that all mainstream TIFF developers should support in their products. Conformance to TIFF format is subject to adherence of the Baseline TIFF requirements. These requirements are well documented in the specifications document 6.0.

#### Multiple Images Per File ####

There may be more than one IFD in a TIFF file. Each IFD defines a subfile. One potential use of subfiles is to describe related images, such as the pages of a fac- simile transmission. A Baseline TIFF reader is not required to read any IFDs beyond the first one.

#### Image Types ####

Baseline TIFF Image has following types:

**Bilevel:** A bilevel image contains two colors—black and white. TIFF allows an application to write out bilevel data in either a white-is-zero or black-is-zero format. The field that records this information is called **PhotometricInterpretation**.

* RGB full-color

PhotometricInterpretation information for Bilevel images is as follow:

Tag = 262  (106.H)
Type = SHORT
**Values**

|Value|Decription|
---|---|
|0|For bilevel and grayscale images:  0 is imaged as white. The maxi-mum value is imaged as black. This is the normal value for Compression#2|
|1|BlackIsZero. For bilevel and grayscale images:  0 is imaged as black. The maxi-mum value is imaged as white. If this value is specified for Compression#2, theimage should display and print reversed.|

**GrayScale:** Grayscale images are a generalization of bilevel images. Bilevel images can store only black and white image data, but grayscale images can also store shades of gray. To describe such images, you must add or change the following fields. The other required fields are the same as those required for bilevel images. For grayscale images, Compression # 1 or 32773 (PackBits). In Baseline TIFF, grayscale images can either be stored as uncompressed data or compressed with the PackBits algorithm.

**BitsPerSample** information for grayscale images is as follow:

Tag = 258  (102.H)
Type = SHORT

The number of bits per component.Allowable values for Baseline TIFF grayscale images are 4 and 8, allowing either16 or 256 distinct shades of gray.

**Palette-Color:** Palette-color images are similar to grayscale images. They still have one component per pixel, but the component value is used as an index into a full RGB-lookup table. To describe such images, you need to add or change the following fields.The other required fields are the same as those for grayscale images.
PhotometricInterpretation information for Palette-Color image is as follow:

PhotometricInterpretation = 3 (Palette Color).
ColorMapTag = 320 (140.H)
Type = SHORT
N = 3 * (2 BitsPerSample)

This field defines a Red-Green-Blue color map (often called a lookup table) for palette color images. In a palette-color image, a pixel value is used to index into an RGB-lookup table. For example, a palette-color pixel having a value of 0 would be displayed according to the 0th Red, Green, Blue triplet.In a TIFF ColorMap, all the Red values come first, followed by the Green values,then the Blue values. In the ColorMap, black is represented by 0,0,0 and white is represented by 65535, 65535, 65535.

**RGB full-color:** In an RGB image, each pixel is made up of three components: red, green, and blue. There is no ColorMap.To describe an RGB image, you need to add or change the following fields and values. The other required fields are the same as those required for palette-color images.

BitsPerSample = 8,8,8. Each component is 8 bits deep in a Baseline TIFF RGB image.

PhotometricInterpretation = 2 (RGB) and there is no ColorMap.

Tag = 277  (115.H)
Type = SHORT
The number of components per pixel. This number is 3 for RGB images, unless extra samples are present.

## References ##

* [TIFF File Format - Wikipedia](https://en.wikipedia.org/wiki/TIFF)
