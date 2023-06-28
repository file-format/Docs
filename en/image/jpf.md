{
  "date" : "2021-02-10",
  "keywords" : [ "jpf file", "jpf file format", "what is a jpf file", "file", "jpf example", "jpf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JPF - Image File Format",
  "description":"Learn about JPF file format and APIs that can create and open JPF files.",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-02-10"
}

## What is a JPF file? ##

A file with .jpf extension is an extension to the JPEG 2000 image coding system ISO/IEC 15444 and is referred to as its Part 2 ISO/IEC 15444-2. It defines and specifies a set of lossless (bit-preserving) and lossy compression methods for coding continuous-tone, bi-level, grey-scale, colour digital still images, or multi-component images. The first part of ISO/IEC 15444-1 is referred to the [JP2](/image/jp2/) that uses the wavelet technology to code lossless content and is the base for JPEG 2000 image file formats. The JPF file format didn't receive a warm reception due to the extensive usage of JPEG format. JPF files can be opened with popular imaging applications such as Adobe Photoshop 2020, Adobe Illustrator 2020, and CorelDraw Graphics Suite 2020.

## Brief History

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees. In the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. In 2004, the ISO/IEC 15444-2 format was publicly accepted as extension to the JP2 file format.

## JPF File Format

The JPF file format defines extended decoding processes for conversion of compressed image data for reconstruction.  It is an extended file format that specifies extended codestream syntax containing information for interpreting the compressed image data. This extended standard specifies a container to store image metadata and provides guidance on extended encoding processes for converting source image data to compressed image data.

### File Organization

JPF is the formal storage file format when JPX files are stored in computer file systems. In addition, other Recommendations/ International Standards may define other boxes for use within JPX files. However, all information contained within a JPX file shall be in the box format; byte-streams not in the box format shall not be found in the file. The binary structure of a box in a JPX file is identical to that defined in the [JP2](/image/jp2/) file format.

## References ##

* [Overview of JPEG 2000](https://jpeg.org/jpeg2000/)
* [ISO/IEC 15444-2:2004](https://www.iso.org/standard/33160.html)
