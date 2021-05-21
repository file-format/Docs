---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF File Format
linktitle: JFIF
description: Learn about JFIF file format and APIs that can create and open JFIF files.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## What is a JFIF file? ##

JFIF (JPEG File Interchange Format (JFIF)) is an image format file that uses the .jfif extension. JFIF builds over JIF (JPEG Interchange Format) by reducing complexity and solving its limitations.

## Brief History ##

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. Version 1.02 was published on September 7, 1992. RFC 2046 specified that the JFIF format is used to transmit JPEG images over the internet. JFIF was published by ECMA in 2009 and was standardized by ITU-T in 2011 as its Recommendation T.871 and by ISO/IEC in 2013 as ISO/IEC 10918-5

## JFIF Design ##

JFIF allows multiple components like Y, Cb, Cr, to have different resolutions but their alignment is not defined. Unlike JPEG, JFIF can provide resolution and aspect ratio information. JFIF also defines the color model to be used.

## JFIF File Format ##

A JFIF file consists of a sequence of markers as defined in part 1 of the JPEG Standard. Each marker consists of two bytes (FF followed by a byte that specifies the type of marker). Markers can either be stand-alone or indicate the start of a marker segment.

### File Structure ##

|Segment|Code|Description|
|---|---|---|
|SOI|FF D8|Start of Image|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|additional marker segments|
|SOS|FF DA|Start of Scan|
||compressed image data||
|EOI|FF D9|End of Image|

The JFIF Standard defines the following segments:

### JFIF APP0 marker segment ###

It is a mandatory segment containing image parameters. It can also contain an embedded uncompressed thumbnail.

|Field|Size (bytes)|Description|
|---|---|---|
|APP0 marker|2|FF E0|
|Length|2|Length of segment excluding APP0 marker|
|Identifier|5|JFIF (4A 46 49 46 00) in ASCII terminated by a null byte|
|JFIF version|2|Version of the JFIF|
|Density units|1|Unit for the following pixel density fields</br> 00 : No units; width:height pixel aspect ratio is equal to Ydensity:Xdensity </br> 01 : Pixels per inch </br>02 : Pixels per centimeter|
|Xdensity|2|Horizontal pixel density greater than zero|
|Ydensity|2|Vertical pixel density greater than zero|
|Xthumbnail|1|Horizontal pixel count of the embedded RGB thumbnail. May be zero|
|Ythumbnail|1|Vertical pixel count of the  embedded RGB thumbnail. May be zero|
|Thumbnail data|3 × n|Uncompressed 24 bit RGB raster thumbnail data|

### JFIF extension APP0 marker segment ###

This is an optional section that if defined, must immediately follow the JFIF APP0 marker segment. This section is supported by JFIF version 1.02 and above and allows the embedding of thumbnails in three different formats.

|Field|Size (bytes)|Description|
|---|---|---|
|APP0 marker|2|FF E0|
|Length|2|Length of the segment excluding APP0 marker|
|Identifier|5|JFXX (4A 46 58 58 00) in ASCII terminated by a null byte|
|Thumbnail format|1|Specifies what data format is used for the following embedded thumbnail:</br>10 : JPEG format</br>11 : 1 byte per pixel palettized format</br>13 : 3 byte per pixel RGB format|
|Thumbnail data|variable||

## References ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)
