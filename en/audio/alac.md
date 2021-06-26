---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about ALAC file format and APIs that can create and open ALAC files.
title: ALAC - Apple Lossless Audio Codec File Format
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## What is a ALAC file? ##

ALAC file format is Apple Lossless Audio Codec (ALAC) that uses the MPEG-4 compliant QuickTime container. It was introduced in 2004 as proprietary file format, until 2011 when Apple made it available open source and royalty-free. The format is similar to the [FLAC](/audio/flac/) (Free Lossless Audio Codec) but offers more compression comparatively. It offers better sounding alternative to [AAC](/audio/aac/) or [MP3](/audio/mp3/). Audio files encoded with ALAC codec can be opened using Apple QuickTime, Apple iTunes and Micrsoft Windows Media Player with K-Lite codec.

## ALAC File Format

Files based on the ALAC codec are binary files that is available as [open source on GitHub](https://github.com/macosforge/alac) for developer's reference. It contains the sources for the ALAC encoder and decoder. Apple has also provided a command line utility, called `alacconvert`, to read and write the audio data to/from Core Audio Format (CAF) and [WAVE](/audio/wav/) files. Following are some key points about the ALAC file format.

 1. `Bit Depths` - 16, 20, 24 and 32 bits.
 1. `Sample Rate` - Any arbitrary integer sample rate from 1 to 384,000 Hz. Theoretical rates of up to 4,294,967,295 (2^32 - 1) Hz could be supported.
 1. `Packet Size` - The default packet size defaults to 4096 sample frames of audio per packet. Other packet sizes are certainly possible. However, non-default packet sizes are not guaranteed to work properly on all hardware devices that support Apple Lossless. Packets above 16,384 sample frames are not supported.
 1. `Supported Channels` - It supports one to eight channels. Each channel has the following order of information.

 |Num Chan|	Order|
 |---|---|
 |1 		|mono|
 |2 		|stereo (Left, Right)|
 |3 		|MPEG 3.0 B (Center, Left, Right)|
 |4 		|MPEG 4.0 B (Center, Left, Right, Center Surround)|
 |5 		|MPEG 5.0 D (Center, Left, Right, Left Surround, Right Surround)|
 |6 		|MPEG 5.1 D (Center, Left, Right, Left Surround, Right Surround, Low Frequency Effects)|
 |7 		|Apple AAC 6.1 (Center, Left, Right, Left Surround, Right Surround, Center Surround, Low Frequency Effects)|
 |8 		|MPEG 7.1 B (Center, Left Center, Right Center, Left, Right, Left Surround, Right Surround,  Low Frequency Effects)|

## References

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac on GitHub](https://github.com/macosforge/alac)
