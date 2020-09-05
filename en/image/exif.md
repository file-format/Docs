{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EXIF",
  "description":"Learn about EXIF file format and APIs that can create and open EXIF files.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is an EXIF file? #

EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. The standard is managed by Japan Electronics and Information Technology Industries Association (JEITA) as of today.  EXIF is a standard for the specifications of image and sound formats mainly used by digital cameras and scanners.

EXIF standard includes the tagging and metadata information with the image file. Metadata can contain information like camera model, shutter speed, Date and time, aperture, manufacturer, exposure time, X resolution, Y resolution etc. Normally the EXIF data is hidden by default. In order to view the EXIF data, one has to select the view properties within image viewing application. Exif metadata may also include thumbnails along with technical and primary image data in a single image file.

## History and Versions ##

* In Oct 1995, JEIDA established Version 1. In this version JEIDA defined the structure, which consists of image data format and attribute information, and basic tags.
* Nov 1997, version 1.1 was introduced with most of the tags from version 1 but also added provisions for optional attribute information and format operation.
* June 1998, Version 2 with sRGB colour space, compressed thumbnails and audio files.
* December 1998, Version 2.1 with enhanced storage and attribute information.
* February 2002, Version 2.2, improved version 2.1 with the addition of print finishing.
* September 2003, Version 2.21 with optional colour space known as adobe RGB.

## File Format Information ##

EXIF uses the following file formats with the addition of specific metadata.

1. [JPEG](/image/jpeg/) - discrete cosine transform (DCT) for compressed image files.
1. [TIFF](/image/tiff/) Rev. 6.0 (RGB or YCbCr) for uncompressed image files.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) for audio files (Linear [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) or ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM for uncompressed audio data, and [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) for compressed audio data). 

### Marker used by EXIF ###

The marker 0xFFE0~~0xFFEF is "Application Marker", used by user application. For example, older digi cams use JFIF (JPEG File Interchange Format) for storing images. JFIF uses APP0 (0xFFE0) Marker for inserting digi cam configuration data and thumbnail image. Furthermore, EXIF also uses an Application Marker for inserting data, but EXIF uses APP1 (0xFFE1) Marker to avoid a conflict with JFIF format. Every EXIF file formats starts from this format.


|SOI Marker|APP1 Marker|APP1 Data|Other Marker
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

It starts from SOI (0xFFD8) Marker, so it's a JPEG file. Then APP1 Marker follows immediately. All the data of EXIF are stored in this APP1 data area. The part of "SSSS" on upper table means the size of APP1 data area (EXIF data area). Please notice that the size "SSSS" includes the size of descriptor itself also. After the "SSSS", APP1 data starts. The first part is a special data for the identification whether EXIF or not, ASCII character "EXIF" and 2 bytes of 0x00 are used. After the APP1 Marker area, the other JPEG Markers follows.

### Exif Data Structure ###

A Rough structure of EXIF data (APP1) is shown as below. As discussed above, EXIF data starts from ASCII character "EXIF" and 2 bytes of 0x00, then EXIF data follows. EXIF uses TIFF format to store data.


|FFE1|APP1 Marker
---|---|
|SSSS|APP1 Data|APP1 Data Size
|45786966 0000|Exif Header
|49492A00 08000000|TIFF Header
|XXXX. . . .|IFD0 (main image)|Directory
|LLLLLLLL|Link to IFD1
|XXXX. . . .|Data area of IFD0
|XXXX. . . .|Exif SubIFD|Directory
|00000000|End of Link
|XXXX. . . .|Data area of Exif SubIFD
|XXXX. . . .|IFD1(thumbnail image)|Directory
|00000000|End of Link
|XXXX. . . .|Data area of IFD1
|FFD8XXXX. . . XXXXFFD9|Thumbnail image

#### TIFF Header ####

he 8-byte [TIFF](/image/tiff/) file header contains the following information:

`Bytes 0-1:`  The byte order used within the file. Legal values are:“II”(4949.H)“MM”  (4D4D.H).

In the “II” format, byte order is always from the least significant byte to the most significant byte, for both 16-bit and 32-bit integers This is called little-endian byte order. In the “MM” format, byte order is always from most significant to least significant, for both 16-bit and 32-bit integers. This is called big-endian byte order.

`Bytes 2-3:`   An arbitrary but carefully chosen number (42) that further identifies the file as a TIFF file.The byte order depends on the value of Bytes 0-1.

`Bytes 4-7:`    The offset (in bytes) of the first IFD. The directory may be at any location in the file after the header but must begin on a word boundary. In particular, an Image File Directory may follow the image data it describes. Readers must follow the pointers wherever they may lead.The term byte offset is always used in this document to refer to a location with respect to the beginning of the TIFF file. The first byte of the file has an offset of 0.

#### Image File Directory ####

An IFD contains information about the image as well as pointers to the actual image data.. It consists of a 2-byte count of the number of directory entries (i.e. the number of fields), followed by a sequence of 12-byte field entries, followed by a 4-byte offset of the next IFD (or 0 if none). There must be at least 1 IFD in a TIFF file and each IFD must have at least one entry.

##### IFD Entry #####

Each 12-byte IFD Entry is in the following format.


|Bytes|Description
---|---|
|0-1|The Tag that identifies the field
|2-3|The field type
|4-7|Count of the indicated type
|8-11|The Value Offset, the file offset (in bytes) of the Value for the field.The Value is expected to begin on a word boundary; the correspond-ing Value Offset will thus be an even number. This file offset maypoint anywhere in the file, even after the image data

A TIFF field is a logical entity consisting of TIFF tag and its value. This logical concept is implemented as an IFD Entry, plus the actual value if it doesn’t fit into the value/offset part, the last 4 bytes of the IFD Entry. The terms TIFF field and IFD entry are interchangeable in most contexts.

#### Thumbnail Image ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. There are 3 formats for thumbnails; JPEG format(JPEG uses YCbCr), RGB TIFF format, YCbCr TIFF format.

##### JPEG Format Thumbnail #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. It seems that JPEG format and 160x120pixels of size are recommended thumbnail format for Exif2.1 or later.

##### TIFF Format Thumbnail #####

If the value of Compression(0x0103) Tag in IFD1 is '1', thumbnail image format is no compression(called TIFF image). Start point of thumbnail data is StripOffset(0x0111) Tag, size of thumbnail is the sum ofStripByteCounts(0x0117) Tag.

## References ##

* [EXIF - By Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [EXIF File Format](https://www.media.mit.edu/pia/Research/deepview/exif.html)
