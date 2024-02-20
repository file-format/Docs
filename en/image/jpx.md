{
  "date": "2021-02-10",
  "keywords": [
    "jpx file",
    "jpx file format",
    "what is a jpx file",
    "file",
    "jpx example",
    "jpx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "JPX - Image File Format",
  "description": "Learn about JPX file format and APIs that can create and open JPX files.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpx"
    }
  },
  "lastmod": "2021-02-10"
}

## What is a JPX file? ##

A file with .jpx extension is an extension to the JPEG 2000 file format. It uses the JPEG 2000 compression primarily and also provides advanced features such as multiple layers for an image, various colour spaces, opacity, and fragmented code streams. JPX also allows other compressions such as JBIG, CCITT Group3, CCITT Group4, etc. in addition to the JPEG 2000 compression. The JPX file format was approved as [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standard, but couldn't receive a warm reception due to the extensive usage of [JPEG](/image/jpeg/) file format. Applications that can open JPX files include Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020, and CorelDraw Graphics Suite 2020.

## Brief History

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. In 2004, the ISO/IEC 15444-2 format was publicly accepted as extension to the JP2 file format.

## JPX File Format

The JPX file format was formulated to meet the requirements of applications that were in need of data structures beyond the functionality defined by the [JP2](/image/jp2/) file format. A JP2 file with non-compatible extensions could lead to confusion in the marketplace where some readers can interpret some JP2 files but not others. JPX is the answer to avoiding such issues in applications.

### File Identification

JPX files are stored as [JPF](/image/jpf/) when stored in traditional computer file system. That is why JPX term is least commonly used as compared to the JPF. A JPX file begins with the following bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### File Organization

Similar to JP2, a JPX file is a collection of boxes having a binary structure with the boxes arranged in a contiguous order. The first box gives the start to the file with its first byte and the last byte of the last box represents the last byte of the file.
The binary structure of a box in a JPX file is identical to that defined in the [JP2](/image/jp2/) file format.

### Storage of CodeStream in JPX

The JPX file format allows the image codestream to be divided into fragments. This makes it possible to modify a single tile of the image and write the modified tile to the end of the file without rewriting the entire file. The original [JP2](/image/jp2/) file format restricts the entire codestream to be stored in a contiguous portion of the file, that can be problematic for image editing applications that may desire to modify a single tile of the image and achieve the above supportability by JPX file format. The fragmentation of image codestream makes the JPX file format superior over the JP2 file format. In addition, JPX file format allows multiple codestream to be combined and produce rendered result. Codestreams can be combined as compositing and animation.

## References ##

* [Overview of JPEG 2000](https://jpeg.org/jpeg2000/)
