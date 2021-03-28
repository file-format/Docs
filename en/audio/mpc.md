---
date: 2021-03-21
keywords: mpc, Musepack file format, .mpc extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about MPC file format and APIs that can create and open MPC files.
title: MPC - Musepack Audio Compression File Format
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## What is a MPC file?

A file with .mpc extension is a [Musepack](https://musepack.net/) audio file format that uses audio compression with a strong emphasis on high quality. This makes it possible for you to not even notice the sound quality differences of original [WAV](/audio/wav/) file and the compressed MPC file. It uses MPEG-1 Layer-2 algorithms to achieve highly optimized compression. Musepack MPC file format is open source with BSD/GNU LGPL license. The [SVN repository](http://svn.musepack.net/) by Musepack allows to get latest updated code for the codec. Applications that can open MPC files include VLC Media Player, JetAudio, and Winamp in addition to several others.

## MPC File Format

MPC file uses the MPEG-1 Layer-2 algorithms to compress the audio files. It is a container-independent format and also allows raw stream encoding. The format doesn't use any internal clipping and is streamable with sample-accurate cutting. Its Packetized stream allows multiplexing into audio and video containers such as [MKV](/video/mkv/).

## References

* [Musepack MPC - Wikipedia](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)
