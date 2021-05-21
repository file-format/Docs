---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about VOB file format and APIs that can create and open VOB files.
title: VOB File Format
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## What is a VOB file? ##

VOB files are stored typically in the VIDEO_TS directory on a DVD with a .vob extension. VOB files contain video and audio data as well as other data like menus and subtitles. VOB is based on MPEG-2 program stream format but it has additional limitations and specifications in private streams. VOB files are a strict subset of MPEG program streams so all VOB files are MPEG program streams but all MPEG program streams are not VOB compliant.

## Structure of DVD Video ##

When a DVD is opened on a computer, VIDEO_TS is the top level directory with AUDIO_TS. AUDIO_TS is empty and is not used. Inside the VIDEO_TS directory, there are VOB, BUP, and IFO files. VOB files contain the MPEG content. These are broken into 1 GB or less sized chunks so that these are compatible with all the operating systems. The IFO files contain information regarding the menus and the title structure. The BUK files are backup files of the IFO files with the same name. These files are meant to be kept in a separate area physically so that in case the IFO file is damaged due to physical damage to the DVD, the BUK file can provide the same information.

### Physical Layout ###

- All files on the disk must be contiguous.
- The related files should be next to each other(VOB, IFO, BUP).
- The numbered files should be in ascending order.

## Copy Protection ##

Many video DVDs are encrypted and prevent the copying of data from the DVD. Authentication and decryptions keys are needed to play the files which are located in the inaccessible lead-in area of the DVD. These keys are used by the CSS decryption software that is present in the DVD player or the software player. Without the keys, the video files cannot be played as the keys will be requested when the files are opened.

## References ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)
