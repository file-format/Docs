---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF File Format
linktitle: FLIF
description: Learn about FLIF file format and APIs that can create and open FLIF files.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## What is a FLIF file? ##

FLIF (Free Lossless Image Format) is a lossless image format that uses the .flif extension for its files. FLIF claims to outperform [PNG](/image/png/), lossless [WebP](/image/webp/), lossless BPG, and lossless JPEG 2000 in terms of compression ratio. FLIF uses progressive interlacing, due to which any partial download of the image can be used as a lossy encoding for the entire image.

## Brief History ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. In September 2016, the first stable version of FLIF was released.

## FLIF Design ##

FLIF uses a variant of CABAC (Context-adaptive binary arithmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) for compression. MANIAC is an entropy coding algorithm developed by Jon Sneyers and Pieter Wuille. In MANIAC, the contexts are nodes of decision trees that are learned at encoding time dynamically. This makes the context model more image-specific and results in a better compression. FLIF has the following features:

- Supports lossless compression
- Supports lossy compression with encoder preprocessing
- Supports Greyscale, RGB and RGBA
- Supports color depth of 1 to 16 bits per channel
- Supports interlaced and non-interlaced files
- Supports progressive decoding of partially downloaded files
- Supports animations
- Supports embedded ICC color profiles, Exif and XMP metadata
- Has limited support for compressing camera raw files (RGGB)

## FLIF File Format ##

A FLIF file has the following four parts:

## Main Header ##

The main header contains the main metadata including the width, height, color depth, number of frames.

|Type|Value|Description|
|---|---|---|
|4 bytes|"FLIF"|Magic|
|4 bits|3 = ni still; 4 = i still; 5 = ni anim; 6 = i anim|Interlacing, animation|
|4 bits|1 = Grayscale; 3 = RGB; 4 = RGBA|Number of channels (nb_channels)|
|1 byte|'0','1','2' ('0'=custom)|Bytes per channel (Bpc)|
|varint|width-1|Width|
|varint|height-1|Height|
|varint|nb_frames-2 (only if animation)|Number of frames (nb_frames)|

## Metadata chunks ##

This part contains non-pixel like Exif/XMP metadata, ICC color profile, etc. that is encoded using DEFLATE compression. These chunks are defined similarly to PNG chunks with the difference being that the chuck size is encoded with a variable number of bytes. Chunks' names can be 4 letters (4 bytes) or a value below 32 indicating a non-optional chunk.

The following is an example of optional chucks:

|Chunk name|Description|Content (after DEFLATE-decompression)|
|---|---|---|
|iCCP|ICC color profile|raw ICC color profile data|
|eXif|Exif metadata|"Exif\0\0" header followed by a TIFF header and the EXIF data|
|eXmp|XMP metadata|XMP contained within a read-only xpacket with no padding|

### Naming Convention ###

- **First Letter**: Uppercase is used for critical and lowercase is used for non-critical chunks.
- **Second Letter**: Uppercase is used for public and lowercase is used for private chunks
- **Third Letter**: Uppercase is used for chucks that are needed to display the image correctly and lowercase are not important to display the image.
- **Fourth Letter**: Uppercase is used for chucks that can be safely copied blindly. Lowercase chucks depend on the image data.

## Second Header ##

This contains the information regarding the actual encoding of the pixels.

|Type|Description|Condition|Default Value|
|---|---|---|---|
|1 byte|NUL byte (0x00), chunk name of a FLIF16 bitstream||
|uni_int(1,16)|Bits per pixel of the channels|Bpc == '0': repeat(nb_channels)|8 if Bpc == '1', 16 if Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Number of loops|nb_frames > 1||
|uni_int(0,60_000)|Frame delay in ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flag: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alpha divisor|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Flag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variable|Transformations (see below)|||
|uni_int(1) = 0|Indicator bit: done with transformations|||
|uni_int(0,2)|Invisible pixel predictor|alpha_zero && interlaced && alpha range includes zero||

**Channels**

|Channel number|Description|
|---|----|
|0|Red or Gray|
|1|Green|
|2|Blue|
|3|Alpha|

**Transformations**

|Type|Description|
|---|---|
|uni_int(1) = 1|Indicator bit: not done yet|
|uni_int(0,13)|Transformation identifier|
|variable|Transformation data (depends on transformation)|

Transformation is used to modify pixel data for better compression and to keep track of actually occurring pixel values.

## Pixel Data ##

This part contains the actual pixel data encoded using MANIAC entropy coding. The pixels may be encoded using interlaced or non-interlaced encoding.

### Interlaced method ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. In other words, every even-numbered zoomlevel 2k is a downsampled version of the image, at scale 1:2^k. Zoomlevels are encoded from the highest to the lowest.

### Non-interlaced method ###

In this method, the encoding of the MANIAC trees begins immediately followed by the encoding of the pixels.

## How to open FLIF files ##

You may use the following programs to open FLIF files.

- ImageMagick
- XnView

## References ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)
