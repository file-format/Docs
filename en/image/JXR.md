---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR File Format
linktitle: JXR
description: Learn about JXR file format and APIs that can create and open JXR files.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## What is a JXR file? ##

JPEG XR (JPEG extended range) is a file format for continuous tone photographic images. It is a still-image compression standard that is based on HD Photo developed by Microsoft. It supports both lossy and lossless compression.

## Brief History ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. It was renamed HD Photo in November 2006. JPEG XR was approved as International Standard ISO/IEC 29199-2 on 19 June 2009. The ITU-T and ISO/IEC published a motion format specification (ITU-T T.833 | ISO/IEC 29199-3), a conformance test set (ITU-T T.834 | ISO/IEC 29199-4), and reference software (ITU-T T.835 | ISO/IEC 29199-5) for JPEG XR after the completion of the image coding specification in 2010. A technical report describing the workflow architecture for JPEG XR was published in 2011.

## JPEG XR Design ##

As compared to JPEG, JPEG XR offers several improvements including:

- **Better Compression**: JPEG XR offers higher compression ratios.
- **Lossless Compression**: JPEG XR supports lossless compression.
- **Tile Structure**: JPEG XR image can be segmented into tile regions where each region can be decoded separately.
- **More color accuracy**: JPEG XR includes internal conversion to the YCoCg color space for supporting images using RGB color space. JPEG XR also supports a 16-bit per component (64-bit per pixel) integer CMYK color model. JPEG XR supports RGBE shared-exponent floating point color format for HDR images. JPEG XR supports grayscale and multi-channel color encodings as well.
- **Transparency Map**: JPEG XR supports the alpha channel for transparency.
- **Compressed-domain image modification**: JPEG XR images can be converted to lossy encoding, reduced in resolution, cropped, flipped, rotated, and the tile structure can be altered  all without full decoding of the file.
- **Metadata Support**: JPEG XR image file may contain ICC color profile for consistent color representation across multiple devices. The format also supports Exif and XMP metadata formats.

## Container Format ##

JPEG XR image data can be stored in TIFF-like container format by using a table of Image File Directory (IFT) tags. A JXR file contains the following in IFD tags:

- Image data: It is a contiguous self-contained image data.
- Optional alpha channel data: If this is present, the image data can be compressed separately enabling the support of applications that do not support transparency.
- Metadata
- Optional XMP metadata
- Optional Exif metadata

As it is based on TIFF format, it inherits all of the TIFF format limitations like the 4 GB file size limit.

## References ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)
