---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ File Format
linktitle: ARJ
description: Learn about ARJ file format and APIs that can create and open ARJ files.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## What is an ARJ file? ##

ARJ (Archived by Robert Jung) is a high efficiency compressed archive file developed by Robert K. Jung. ARJ was developed for DOS and early versions of Windows in the early 1990s. ARJ files are useful for backing up or sharing a large number of files as you do not have to keep track of all those files and there is only a single file to handle. The .arj extension is used for the ARJ archive files.

## ARJ File Format ##

An ARJ file contains two types of headers:

- Main header: There is one main header at the start of the archive.
- Local headers: Local headers are present before each file.

|Offset|Type|Count|Description|
|---|---|---|---|
|0000h|word|1|ID=0EA60h|
|0002h|word|1|basic header size|
|0004h|byte|1|Size of header|
|0005h|byte|1|Archiver version number|
|0006h|byte|1|Minimum version number needed|
|0007h|byte|1|Host OS: </br>0 - MS-DOS</br>1 - PRIMOS</br>2 - UNIX</br>3 - AMIGA</br>4 - MAC-OS (System xx)</br>5 - OS/2</br>6 - APPLE GS</br>7 - ATARI ST</br>8 - NeXT</br>9 - VAX VMS|
|0008h|byte|1|Internal Flags, bitmapped: </br>0 - no password / password</br>1 - reserved</br>2 - file continues on next disk</br>3 - file start position field is available</br>4 - path translation ( "\" to "/" )|
|0009h|byte|1|Compression method: </br>0 - stored</br>1 - compressed most</br>2 - compressed</br>3 - compressed faster</br>4 - compressed fastest|
|000Ah|byte|1|File type: </br>0 - binary</br>1 - 7-bit text</br>2 - comment header</br>3 - directory</br>4 - volume label|
|000Bh|byte|1|reserved|
|000Ch|dword|1|Date/Time of original file in MS-DOS format|
|0010h|dword|1|Size of the compressed file|
|0014h|dword|1|Size of the original file"|
|0018h|dword|1|CRC-32 of the original file|
|001Ah|word|1|Filespec position in filename|
|001Ch|word|1|File attributes|
|001Eh|word|1|Host data|
|?|dword|1|Extended file starting position|
|????h|dword|1|CRC-32 of the basic header|
|????h|word|1|Size of the first extended header|
|????h+"SIZ"+2|dword|1|CRC-32 of the extended header|
|????h+"SIZ"+6|byte|?|Compressed file|

## References ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)
