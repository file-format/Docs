---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about F4V file format and APIs that can create and open F4V files
title: F4V File Format
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## What is an F4V file? ##

F4V (Flash MP4 Video File) is a video file saved with the .f4v extension. It is based on the ISO base media file format (MPEG-4 Part 12). It is very similar to [MP4](/video/mp4/) which is why it is also referred to as the Flash MP4 informally. [FLV](/video/flv/) had limitations when streaming H.264/ACC contents which resulted in Adobe Systems to create the new F4V format. Flash Player can play F4V files since the release of Flash Player 9 Update 3.

## Structure of F4V files ##

F4V file format is based on the ISO base media file format (MPEG-4 Part 12) and is very similar to the MP4 format. For the details regarding the structure, please see the [MP4](/video/mp4/) page. The major difference between F4V and MP4 is the metadata formats that F4V can store. Given below is the list of the metadata formats supported by the F4V format.

- **Tag box**: Additional four optional tag boxes (auth, titl, dscp, cprt) within the Movie (moov) box.
- **XMP Metadata box**: This box comes right after the Movie (moov) box. With this, the file can communicate XMP metadata to an SWF movie through ActionScript.
- **ilst box**: This box occurs inside the Meta (meta) box and can contain a number of metadata tags. The supported data types are given below.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata box**: The text samples (text or tx3g) inside the Media Data box (mdat). It can contain the following metadata boxes.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## How to play F4V files ##

F4V is a popular format and many programs can open it. Given below is a list of some of the programs that can open F4V files.

- Flash Player (as of version 9 update 3)
- VLC Media Player
- F4V Player
- KM Player
- Pot Player

## References ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)
- [Adobe Flash Video File Format Specification Version 10.1](http://download.macromedia.com/f4v/video_file_format_spec_v10_1.pdf)
