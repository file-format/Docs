---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about OGG file format and APIs that can create and open OGG files.
title: OGG File - Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## What is an OGG file? ##

OGG is an Ogg Vorbis Compressed Audio File that is saved with the .ogg extension. OGG files are used for storing audio data and can include artist and track information and metadata as well. OGG is a free and open container format that is maintained by Xiph.Org Foundation.

## Brief History ##

Ogg project started as a part of a larger project in 1993 and was named Squish but because of an existing trademark, it was renamed to OggSquish. It was described as an attempt to create a flexible compressed audio format for modern audio applications. OGG reference was separated from Vorbis on September 2, 2000.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. By June 30, 2009, OGG was the only container format supported by the HTML5 implementation of Firefox 3.5.

## OGG File Format ##

The OGG format consists of chunks of data. Each chunk is called an Ogg page. Each page begins with "OggS" to identify Ogg Format. The header contains the serial number and page number that identifies each page as a part of a series. The page consists of the following components.

- **Page Header**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

     | Bit | Value | Description |
      | --- | --- | --- |
      | 0 | 0x01 | Indicates that the first packet of the page is the continuation of the previous packet in the logical bitstream. |
      | 1 | 0x02 | Indicates that this page is the first in the logical bitstream. |
      | 2 | 0x04 | Indicates that this page is the last in the logical bitstream. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadata**: VorbisComment is the most widely-supported mechanism for storing metadata. Other mechanisms include the following:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## References ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)
