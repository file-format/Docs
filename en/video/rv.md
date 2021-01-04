---
date: 2019-10-11
keywords: rv, .rv, rv file format, .rv file format, .rv extension,  rv video format, RealVideo file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about RV file format and APIs that can create and open RV files.
title: RV File Format
linktitle: RV
menu:
  docs:
    parent: "video"
lastmod: 2020-30-12
---

## What is an RV file? ##

RealVideo (RV) is a proprietary video format developed by RealNetworks and released in 1997. The RealVideo files are stored with the .rv extension. RealVideo is supported on multiple platforms like Windows, Mac, Linux, etc.

Usually, RealVideo is paired with [RealAudio (RA)](/audio/ra/) in the [RealMedia (RM)](/video/rm/) container. It is suitable for streaming content over the internet and can be used for streaming live television for example.

## Technology ##

The first version of RealVideo announced in 1997 was based on the H.263 format. RealNetworks continued to use the H.263 until the release of RealVideo version 8 when they switched to a proprietary video format.

RealVideo can be played from a RealMedia file or can be streamed over the internet by using the Real Time Streaming Protocol (RSTP). RSTP is used to manage the connection, to send the actual data, the Real Data Transport (RDT) protocol is used.

For real-time streaming, RealVideo uses a constant bit rate encoding. RealNetworks recently introduced a variable bit rate variant of RealMedia as [RealMedia Variable Bitrate (RMVB)](/video/rmvb/). RMVB allows for the better video quality but is less suited for streaming as network capacity cannot be predicted.

## Video compression formats and codecs ##

RealVideo is comprised of different video compression formats each identified by a four-character code. Given below is a list of video compression formats and the version of RealVideo that introduced them.

|Video compression format|RealVideo Version|
|---|---|
|RV10|1.0|
|RV20|RealVideo G2 and RealVideo G2+SVT|
|RV30|8|
|RV40|9,10|
|RV60|11|

## How to play RV files ##

The official player for RealVideo is RealPlayer developed by RealNetworks. As the format is not open source, other players rely on dynamically linked libraries (DLLs) from the official RealPlayer to play the files. That means that the RealPlayer should be installed on the user's machine for many of these third party players. RealNetworks also developed the open-source Helix player that can play some of the RealVideo files. The programs supporting FFmpeg can also play RealVideo files.

Here a is list of some of the players that can play RV files.

- RealPlayer
- RealOne Player
- KMPlayer
- Zoom Player
- Media Player Classic (with Real Alternative component)
- Microsoft Windows Media Player (with Real Alternative component)

## References ##

- [RealVideo - Wikipedia](https://en.wikipedia.org/wiki/RealVideo)
