---
date: 2020-08-12
keywords: bpg, .bpg, bpg file format, how to open bpg files, .bpg extension, bpg extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG File Format
linktitle: BPG
description: Learn about BPG file format and APIs that can create and open BPG files.
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## What is a BPG file? ##

BPG (Better Portable Graphics) is a file format created by Fabrice Bellard in 2014 for digital images. He proposed BPG as a replacement for JPEG as BPG was more compression or size efficient. BPG uses the intra-frame encoding of the HEVC (High-Efficiency Video Coding) video compression standard.

BPG is designed as a portable memory-efficient format to work on handheld and IoT devices. Currently, web browsers do not support BPG format, but websites can still deliver BPG images by using a JavaScript library written by Bellard. BPG uses the HEVC's Main 4:4:4 16 Still Picture profile up to 14 bits per sample.

## Specifications ##

The BPG container format is a generic image format rather than the raw bitstream used in HEVC. BPG supports 4:4:4, 4:2:2, and 4:2:0 color formats. Alpha channel is also supported with a separately coded extra channel or the fourth channel of CMYK image. BPG provides metadata support for Exif, ICC profiles, and XMP. BPG supports YCbCr (ITU-R BT.601, BT.709, and BT.2020 (non-constant luminance)), YCgCo, RGB, CMYK, and grayscale color space. BGP also supports animation and lossy and lossless HEVC data compression.

## How to open BPG files ##

BPG files are supported by the following programs.

- BPGviewer
- Simple BPG Image viewer
- ImageMagick

## References ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)
