{
  "date" : "2019-10-11",
  "keywords" : [ "heic file", "heic file format", "what is a heic file", "file", "heic example", "heic file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HEIC - High-Efficiency Image File Format",
  "description":"Learn about HEIC file format and APIs that can create and open HEIC files.",
  "linktitle" : "HEIC",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-03-29"
}

## What is a HEIC file?

An HEIC file is a High-Efficiency Container Image file format that can store multiple images as a collection in a single file. The format was adopted by Apple as variant of the [HEIF](/image/heif/) with the launch of iOS 11. It was adopted as the default file format for storing images in compressed form on mobile devices. HEIC, like HEIF, are compressed using the High Efficiency Video Coding (HEVC) standard and are smaller in size without compromising the quality.

## HEIC File Format

HEIC is based on the HEIF file format and uses the HEVC standard (also known as H.265) for achieving compact file size without compromising quality. When an image is taken on iOS device (such as IPhone, IPad, or MacOS), it is stored as HEIC file to these devices. HEIC is a container format that can store single or multiple images along with meta data that describes each image. One such example of metadata is [EXIF](/image/exif) that includes the tagging and metadata information with the image file.

### HEIF Data Storage

The HEIF format can store the following types of images and data.

 * Individual images and image thumbnails
 * Sequences of images
 * Post-processing instructions
 * Image metadata, such as [EXIF](/image/exif/) data

HEIF image format provides the capability of several different image formats including [JPEG](/image/jpeg/), [PNG](/image/png/), and [GIF](/image/gif/) at no compromise on image quality.

## Supported Operating Systems

The following operating systems support HEIF content:

 * Android 9 Pie and newer
 * Apple iOS 11 and newer
 * Apple macOS High Sierra and newer
 * Microsoft Windows 10 April 2018 Update (1803) and newer

## References

 * [HEIF - Wikipedia](https://en.wikipedia.org/wiki/High_Efficiency_Image_File_Format)
 * [HEIF information from Nokia Technologies](https://nokiatech.github.io/heif/)
 * [HEIF Reader/Writer Source Code at GitHub](https://github.com/nokiatech/heif)
