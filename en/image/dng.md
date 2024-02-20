{
  "date": "2019-10-11",
  "keywords": [
    "dng file",
    "dng file format",
    "what is a dng file",
    "file",
    "dng example",
    "dng file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DNG - Digital Camera Image File Format",
  "description": "Learn about DNG file format and APIs that can create and open DNG files.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dng"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a DNG file?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. It was basically developed for digital photography. DNG is an extension of [TIFF](/image/tiff/)/EP standard format and uses metadata significantly. In order to manipulate raw data from digital cameras with the ease of flexibility and artistic control, photographers opt camera raw files. JPEG and TIFF formats store images that are processed by the camera, therefore, not much room for alteration is available in such formats.

## History and Versions of DNG File Format

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. Version 1.4.0.0 appeared in 2012.

## DNG File Format

Whereas camera raw files capture unprocessed or low processed data directly from the sensor. As they are similar to film negatives therefore camera raw formats are also known as “Digital Negatives”. Benefit of raw formats is the increased artistic control for the end user. The user can adjust various parameter ranges according to the requirements such as white balance, tone mapping, noise reduction, sharpening and so on. On the other hand camera raw file has to be processed for any use through any software or through a converter.

As there was no standard format available for camera raw files therefore, it created multiple problems for the end user. These problems were addressed by Adobe and defined a non-proprietary format for camera raw files. The format is known as Digital Negative or DNG. DNG can be used by a wide range of hardware and software for the processing of raw files. Furthermore, DNG can also be used as an intermediate format for storing images which were captured originally by camera’s having their own proprietary raw formats.

### DNG File Format Specifications

In this section we will describe the DNG format as an extension of TIFF 6.0.

* **File Extensions**: DNG uses “.DNG” or “.TIF” extensions.
* **SubIFD Trees**: DNG does not support SubIFD chains, instead DNG recommends the use of SubIFD trees as mentioned in TIFF-EP specifications. Highest quality and resolution may use NewSubFileType of 0, while the reduced quality thumbnails should use NewSubFileType equal to 1. It is also recommended though not required that the first IFD must have a low quality or resolution thumbnail.
* **Byte Order**: Byte order must be supported by DNG readers, also for files from a particular camera model.
* **Masked Pixels**:  Most of the camera sensors calculate fully masked pixels at the edge of the sensor through black encoding. These pixels can be either included or trimmed before the image is stored in DNG format. If the masked pixels are not trimmed, then the area of these pixels must be mentioned in the ActiveArea tag. The information gathered from these pixels about black encoding level should be used for either before the raw data is stored or may be included in DNG file specifying the level of black.
* **Defective Pixels**: Before storing raw data as DNG, defective pixels should be excluded.
* **Metadata**: Metadata may be included in DNG in any of the following ways:  
** By using TIFF-EP or EXIF metadata tags
** Through the IPTC metadata tag (33723)
** Using the XMP metadata tag (700)
* **Proprietary Data**: Normally vendors include proprietary data in raw file to be used by their own converters. DNG stores their proprietary data in private tags, private IFDs, and in a private MakerNote. Vendors must use the DNGPrivateData and MakerNoteSafety tags to make sure applications that edit DNG files preserve this proprietary data.

Following are some important restrictions and extensions TIFF tags.

**BitsPerSample**      

8 to 32 bits/sample are supported. There must be same depth for each sample when SamplesPerPixel is not equal to 1.But if BitsPerSample is not equal to 8 or 16 or 32, then bits must be packed into bytes using the TIFF default FillOrder of 1 (big-endian).

**Compression**

Two Compression tag values are supported:

* Value # 1: Uncompressed data.
* Value # 7: JPEG compressed data, either baseline DCT JPEG, or lossless JPEG compression.

**PhotometricInterpretation**

The following values are supported for thumbnail and preview IFDs only:

* 1 = BlackIsZero. Assumed to be in a gamma 2.2 color space.
* 2 = RGB. Assumed to be in the sRGB color space.
* 6 = YCbCr. Used for JPEG encoded preview images.

The following values are supported for the raw IFD, and are assumed to be the camera's native color space:

* 32803 # CFA (Color Filter Array).
* 34892 # LinearRaw.

**Orientation**

Orientation tag is used for file browsers so that they can perform lossless rotation of DNG files. DNG readers must support all possible orientations, including mirrored orientations.

## Features in Latest Version of DNG

DNG Version 1.4 October 2012 has the following advanced features.

* Default User Crop
* Transparency
* Floating Point (HDR)
* Lossy Compression
* Proxies

## References ##

* [DNG Specifications - By Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - The public archival format for digital camera raw data](https://helpx.adobe.com/camera-raw/digital-negative.html)
