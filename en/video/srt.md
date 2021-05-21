---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about SRT file format and APIs that can create and open SRT files.
title: SRT File Format
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## What is an SRT file? ##

SRT (SubRip file format) is a simple subtitle file saved in the SubRip file format with the .srt extension. It contains a sequential number of subtitles, start and end timestamps, and subtitle text. SRT files make it possible to add subtitles to video content after it is produced.

## SRT file Structure ##

Each subtitle has four parts in the SRT file.

1. A numeric counter indicating the number or position of the subtitle.
1. Start and end time of the subtitle separated by --> characters
1. Subtitle text in one or more lines.
1. A blank line indicating the end of the subtitle.

### Example of SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

To specify the time *hours:minutes:seconds,milliseconds (00:00:00,000)* format is used.

## Formatting of SRT files ##

The formatting of SRT files is derived from HTML tags. The formatting tags for the SRT file are listed below.

| Effect | Tags |
| --- | --- |
|Bold|**\<b>...\</b>** or {b}...{/b}|
|Italic|**\<i>...\</i>** or **{i}...{/i}**|
|Underline|**\<u>...\</u>** or **{u}...{/u}**|
|Font Color|**\<font color="white">...\</font>**|
|Line Position|**{\a3}** (indicates that the text should start appearing on line 3)

## SubRip Software ##

SubRip is a free software program that runs on Windows. It extracts subtitles and their timings from different video formats and saves the subtitles in SRT format. SubRip uses optical character recognition to extract subtitles from live video, other video files, and DVDs.

## References ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
- [What is an SRT File? How to Create & Use SRT Files](https://www.rev.com/blog/resources/what-is-an-srt-file-format-create-use-srt-files)
