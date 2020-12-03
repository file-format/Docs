---
date: 2020-24-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format. It is saved with the .mp4 extension.
title: MP4 File Format
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2020-24-11
---

## What is an MP4 file? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Brief History ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. The first version (ISO/IEC 14496-1:2001) of MP4 was a revision of the MPEG-4 Part 1: Systems specification published in 1999. The MP4 file format was generalized to ISO Base Media File Format ISO/IEC 14496-12:2004 that defined the general structure for time-based media files. As a result, it is used as a basis for other file formats.

## Structure of MP4 Files ##

MP4 is an extensible container file, meaning that it does not define a strict structure and allows custom structure and hierarchy for each media type. The data in the MP4 file is divided into two sections, the first containing the media related data and the second containing metadata. The media data contains audio or video and metadata indicate flags for random access, timestamps, etc.
The structures in MP4 are typically referred to as atoms or boxes. The minimum size of an atom is 8 bytes(the first 4 bytes specify size and the next 4 bytes specify type). Here is a list of the root level atoms contained in MP files:

- **ftyp**: Contains the file type, description and the common data structures used.
- **pdin**: Contains progressive video loading/downloading information.
- **moov**: Container for all the movie metadata.
- **moof**: Container with video fragments.
- **mfra**: The container with random access to video fragment
- **mdat**: Data container for media.
- **stts**: sample-to-time table.
- **stsc**: sample-to-chunk table.
- **stsz**: sample sizes (framing)
- **meta**: The container with the metadata information.

Here is a list of second-level atoms used in MP4:

- **mvhd**: Contains the video header information with full details of the video.
- **trak**: Container with the individual track.
- **udta**: The container with the user and track information.
- **iods**: MP4 file descriptor

## How to play MP4 files ##

As MP4 is a standardized video format, almost all the video players out there support it. Given below is a list of some of the video player that can play MP4 files.

- VLC Media Player
- Windows Media Player
- Apple QuickTime Player
- MPlayer

## References ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
- [What Is an MP4 File (and How Do I Open One)?](https://www.howtogeek.com/365037/what-is-an-mp4-file-and-how-do-i-open-one/)
- [MP4 File Format](https://openmp4file.com/format.html)
- [MP4 File Format Specification](https://www.filefix.org/format/mp4.html)
