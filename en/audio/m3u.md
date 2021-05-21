---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about M3U file format and APIs that can create and open M3U files.
title: M3U File Format
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## What is a M3U file? ##

M3U (MP3 URL) is an audio playlist file stored with the .m3u extension. M3U is not an actual audio file, it just points to audio and sometimes video files. M3U was developed to be used with Winplay3 software by Fraunhofer. It is also supported by various media players and software.

## M3U File Format ##

There is no official specification for the M3U file format, it is a de-facto standard. M3U is a plain text file that uses the .m3u extension if the text is encoded in the local system's default non-Unicode encoding or with the .m3u8 extension if the text is UTF-8 encoded. Each entry in the M3U file can be one of the following:

- Absolute path to the file
- File path relative to the M3U file.
- URL

### Extended M3U ###

In the extended M3U, additional directives are introduced that begin with "#" and end with a colon(:) if they have parameters. Given below is a list of directives for extended M3U.

- **#EXTM3U** - It is the file header indicating Extended M3U and must be first line of the file.
- **#EXTENC:** - Text encoding. It must be the 2nd line of the file.
- **#EXTINF:** - Used for track information and other additional properties.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Begin name grouping
- **#EXTALB:** - Album information
- **#EXTART:** - Album artist
- **#EXTGENRE** - Album Genre
- **#EXTM3A** - Single file playlist for album tracks or chapters.
- **#EXTBYT:** - File size in bytes.
- **#EXTBIN:** - Binary data follows.
- **#EXTIMG:** - Logo, Cover or other images.

### HLS M3U ###

HLS (HTTP Live Streaming) was created by Apple to stream audio and radio to iOS devices. It is based on the UTF-8 encoded extended M3U. It was standardized as RFC 8216 in 2017 by IETF. The tags for the HLS playlist begin with "#EXT-X-". Given below is a list of tags for HLS

- **EXT-X-VERSION** - Indicates the compatibility version of the file based on the media and its server.
- **#EXT-X-START:** - Indicates the preferred starting point for the playlist.
- **#EXT-X-PLAYLIST-TYPE:** - Provides the type of playlist (EVENT or VOD).
- **#EXT-X-TARGETDURATION:** - It specifies the maximum Segment duration.
- **#EXT-X-MEDIA-SEQUENCE:** - It indicates the Media Sequence Number.
- **#EXT-X-INDEPENDENT-SEGMENTS** - It indicates that all media samples are independent and can be decoded without other segments.
- **#EXT-X-MEDIA:** - It is used to relate Media Playlists that contain alternative Renditions of the same content.
- **#EXT-X-STREAM-INF:** - It specifies a Variant Stream that is a part of the Renditions.
- **#EXT-X-BYTERANGE:** - Indicates that the Media Segment is a sub-range of the resource identified by its URI.
- **#EXT-X-DISCONTINUITY** - Indicates discontinuity between the preceding and following media segments.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - It allows synchronization between different renditions of the same Variant Stream or different Variant Streams.
- **#EXT-X-KEY:** - Specifies how to decrypt Media Segments.
- **#EXT-X-MAP:** - Specifies how to obtain Media Initialization Section. It is required to parse the applicable Media Segments.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - It associates a Data Range.
- **#EXT-X-I-FRAMES-ONLY** - Indicates that each Media Segment in the Playlist describes a single I-frame.
- **EXT-X-I-FRAME-STREAM-INF** - It indicates that the playlist file contains I-frames of Multimedia presentation.
- **#EXT-X-SESSION-DATA:** - It allows arbitrary session data to be
   carried in a Master Playlist.
- **#EXT-X-SESSION-KEY:** - It allows for encryption keys. The client can preload these keys without reading the playlist first.
- **#EXT-X-ENDLIST** - It indicates that no more Media Segments will be added to the file.

The following is the list of Internet media types used by M3U:

- **application/vnd.apple.mpegurl**: It is the only registered media type (registered in 2009) for M3U that is used to refer to the playlists in HLS applications.
- The following Internet media types are used by non-HLS applications.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U Example ##

This is an example of the M3U file.

```console
#EXTM3U
 
#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3
 
#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## References ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)
