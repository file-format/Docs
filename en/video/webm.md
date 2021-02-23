---
date: 2019-10-11
keywords: WEBM
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about WEBM file format and APIs that can create and open WEBM files.
title: WEBM - WebM Video File Format
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## What is a WEBM file?

A file with .webm extension is a video file based on the open, royalty-free WebM file format. It has been designed for sharing video on the web and defines the file container structure including video and audio formats. WebM is 100% free, implementing high-quality based on the open technologies such as HTML, HTTP, and TCP/IP which are open to anyone for implementation. WebM has been specifically designed for serving video on the web which makes it optimised for streaming with low computational footprint. This makes it suitable for videos playback on any devices specially low-power netbooks, handhelds, and tablets.

## WEBM File Format

The WebM file structure is based on a subset of Matroska [MKV](/video/mkv/) container file format. The video streams available in a WebM file are compressed using the VP8 or VP9 compression technologies that are highly-efficient in compression. Similarly, the audio streams in a WebM file are compressed using the Vorbis or Opus codecs that were developed by the [Xiph Foundation](https://www.xiph.org/). All these video and audio codecs are royalty free and can be used without any charges.

Following are the summarized specifications for the WebM file format.

|Field|Description|
---|---|
|MIME-type	|video/webm|
|Audio-only MIME-type	|audio/webm|
|Uniform Type Identifier|	org.webmproject.webm|
|Video Codec Name|	VP8 or VP9|
|Audio Codec Name|	Vorbis or Opus|

### WebM Elements

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Name	|Description|
---|---|
|EBML|Set the EBML characteristics of the data to follow. Each EBML document has to start with this.|
|EBMLVersion |The version of EBML parser used to create the file.|
|EBMLReadVersion|The minimum EBML version a parser has to support to read this file.|
|EBMLMaxIDLength |The maximum length of the IDs you'll find in this file (4 or less in Matroska).|
|EBMLMaxSizeLength|The maximum length of the sizes you'll find in this file (8 or less in Matroska). This does not override the element size indicated at the beginning of an element. Elements that have an indicated size which is larger than what is allowed by EBMLMaxSizeLength shall be considered invalid.|
|DocType|A string that describes the type of document that follows this EBML header ('webm' in our case).|
|DocTypeVersion|The version of DocType interpreter used to create the file.|
|DocTypeReadVersion|The minimum DocType version an interpreter has to support to read this file.|

#### Global Elements

At the moment, only the `Void` element is supported that is used to void damaged data, to avoid unexpected behaviors when using damaged data. The content is discarded. Also used to reserve space in a sub-element for later use.

#### Segment
This element contains all other top-level (level 1) elements. Typically a Matroska file is composed of 1 segment.

#### Meta Seek Information

The following seeking information is supported.

|Element Name	|Description|
---|---|
|SeekHead |Contains the position of other level 1 elements.|
|Seek |Contains a single seek entry to an EBML element.|
|SeekID |The binary ID corresponding to the element name.|
|SeekPosition |The position of the element in the segment in octets (0 = first level 1 element).|

## References

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)
