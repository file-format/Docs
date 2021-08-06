---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about RM file format and APIs that can create and open RM files.
title: RM File Format
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## What is an RM file? ##

RealMedia is a proprietary multimedia container format developed by RealNetworks that uses the .rm extension. It is used with the combination of [RealAudio (RA)](/audio/ra/) and [RealVideo(RV)](/video/rv/) for streaming over the internet. These streams are of constant bitrate. For variable bitrate, RealNetworks developed the RealMedia Variable Bitrate (RMVB) format. RealMedia is suitable for streaming content over the internet and can be used for streaming live television for example.

## Structure of RealMedia File ##

A RealMedia file consists of a series of chunks, each having the following structure:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

The following are the types of chunks present in the RealMedia file:

- **RealMedia file header (.RMF)**: This must be the first chunk in the RealMedia file. Only one RMF chunk is present in one file. It contains information about the number of headers.
- **File properties header (PROP)**: This contains information about the general properties of the RealMedia file. There is only one chunk of this type in each RealMedia file.
- **Media properties header (MDPR)**: This chunk contains information about the stream properties. It contains information about the type of stream and the codec used. There is one MDPR chunk for each stream in the file.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Data header (DATA)**: This chunk contains a group of data packets.
- **Index header (INDX)**: This chunk comes after all the DATA chunks and contains index entries. One file can have more than one INDX chunks.

## Supported audio and video formats ##

### Audio formats ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- cook: Cook
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Video formats ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 precursor
- RV40: H.264 precursor, RV40
- RVTR: H.263+ (RV20)

## References ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)
