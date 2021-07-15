---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about FLV file format and APIs that can create and open FLV files.
title: FLV File Format
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## What is an FLV file? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe systems created F4V in 2007 due to the restrictions of FLV.

### Encoding ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. Version 8 of Flash Player support for On2 TrueMotion VP6 video bitstreams. It is the recommended compression format for Flash Player 8 and higher. FLV supports audio in MP3, Nellymoser Asao Codec, and the open-source Speex codec. It also supports uncompressed audio or ADPCM format audio. AAC (HE-AAC/AAC SBR, AAC Main Profile, and AAC-LC) are supported by the recent versions of Flash Player 9.

## Structure ##

FLV files consist of Header and Packets. An FLV file starts with the Header. The header has the following fields.

- **Signature**: Its value is FLV
- **Version**: Its default value is 1. Only 0x01 is valid.
- **Flags**: 0x04 is used for audio and 0x01 is used for video so 0x05 is used for both audio and video.
- **Header Size**: The default value is 9. It is used to skip a newer expanded header.

After the header comes the Packets. The FLV file is split into multiple packets called FLV tags that have 15-byte headers. The packets contain the metadata for audio, video, scripts, encryption information, and payload. The FLV packets have the following fields.

- **Reserved**: It is reserved for FMS and should be 0.
- **Filter**: Indicates whether the packets are filtered or not.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: This defines the type of content in the packet.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Data Size**: This denotes the length of the message.
- **Timestamp Lower**: This stores the timestamp in milliseconds at which the tag data applies. It is set to NULL for the first packet.
- **Timestamp Upper**: Extension to create a uint32_be value.
- **Stream ID**: This is set to NULL for the first stream.
- **Payload Data**: This is the data based on the packet type.

## References ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)
