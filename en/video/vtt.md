---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about .vtt file and APIs that can create and open VTT files.
title: VTT File Format - Web Video Text Tracks File
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## What is a VTT file?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT File Format - More information

VTT files use the WebVTT file format for saving sequential text tracks information. Each timed text track consists of a single line or multiple lines, also known as a `cue` as shown in the following example.

### VTT File Example

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT File Structure

Following is the structure requirements of a VTT file.

 * An optional byte order mark (BOM).
 * The string "WEBVTT".
 * An optional text header to the right of WEBVTT.
 * A blank line, which is equivalent to two consecutive newlines.
 * Zero or more cues or comments.
 * Zero or more blank lines.

## References

 * [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 
