---
date: 2019-12-13
keywords: flac, flac file format, .flac extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about FLAC file format and APIs that can create and open FLAC files.
title: FLAC File Format
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2020-24-12
---

## What is a FLAC file? ##

FLAC(Free Lossless Audio Codec) is a lossless compression audio coding format developed by Xiph.Org Foundation. FLAC is a royalty-free open format that is saved with the .flac extension. Digital audio compressed using the FLAC algorithm is typically reduced to 50 to 70 percent in size. FLAC files can be decompressed to an identical copy of the original audio files.

## Brief History ##

Josh Coalson began the development of FLAC in 2000. The first version of FLAC was released on 20 July 2001. FLAC was incorporated under the Xiph.Org flag on 20 January 2003. The development of FLAC was moved to the Xiph.Org git repository with the release of version 1.3.0 on 26 March 2013.

## Composition of FLAC Project ##

The FLAC project consists of the following:

- Stream formats.
- Simple container format for the stream(FLAC).
- libFLAC: A library of reference encoders, decoders, and metadata interface.
- libFLAC++: An object-oriented wrapper for libFLAC.
- flac: A command-line program to encode and decode FLAC streams.
- metaflac: A command-line metadata editor for FLAC.
- Input plugins for music players like Winamp, XMMX, etc.
- Ogg container format (Ogg FLAC).

## FLAC Design ##

Depending on the density and amplitude of the music, the size of the compressed file can be 80% less than the original file.

### Source Encoder ###

- It only supports integer samples and not floating-point. It can handle PCM bit resolution from 4 to 32 bits per sample and sampling rate from 1Hz to 65,535 Hz. FLAC encoding is limited to 24 bits per sample.
- Channels can be grouped to take advantage of interchannel correlations to increase compression.
- CRC checksums are used to identify corrupted frames.
- For conversion of audio samples, FLAC uses linear prediction.

### Metadata ###

- FLAC supports ReplayGain(used to perceive and normalize loudness in audio).
- FLAC uses the same system used in Vorbis comments for tagging.
- libFLAC is used by most FLAC application for encoding/decoding.
- libFLAC API is organized into streams, seekable streams, and files to increase abstraction from base FLAC bitstream.

### Compression ###

libFLAC uses compression levels from 0 to 8 where 0 is the fastest and 8 is the slowest compression level. The compressed files are always lossless although the tradeoff is between speed and size.

## FLAC Format ##

This is an overview of the FLAC bitstream.

- **fLaC marker**: This marker is added to the beginning of the stream. It is followed by one or more metadata blocks.
- **Metadata Blocks**: 128 kinds of metadata blocks are supported by FLAC; currently the following are defined.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: The audio data is composed of one or more audio frames.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## How to Open FLAC Files ##

FLAC files can be opened using the following applications:

- VLC media player
- Microsoft Windows Media Player
- jetAudio
- GoldWave
- VUPlayer

## References ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)
- [FLAC](https://xiph.org/flac/documentation.html)
