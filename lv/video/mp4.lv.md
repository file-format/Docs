---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par MP4 faila formātu un API, kas var izveidot un atvērt MP4 failus.
title: MP4 faila formaat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Kas ir MP4 fails? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Īsa vēsture ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. Pirmā MP4 versija (ISO/IEC 14496-1:2001) bija 1999. gadā publicētās MPEG-4 1. daļas: Sistēmu specifikācijas pārskatīšana. MP4 faila formāts tika vispārināts līdz ISO Base Media File Format ISO/IEC 14496-12. :2004, kas noteica uz laiku balstītu multivides failu vispārējo struktūru. Rezultātā to izmanto par pamatu citiem failu formātiem.

## MP4 failu struktūra ##

MP4 ir paplašināms konteinera fails, kas nozīmē, ka tas nenosaka stingru struktūru un pieļauj pielāgotu struktūru un hierarhiju katram multivides veidam. Dati MP4 failā ir sadalīti divās sadaļās, no kurām pirmā satur ar multividi saistītos datus, bet otrā - metadatus. Multivides datos ir iekļauts audio vai video, un metadati norāda karodziņus nejaušai piekļuvei, laikspiedolus utt.
MP4 struktūras parasti sauc par atomiem vai kastēm. Minimālais atoma izmērs ir 8 baiti (pirmie 4 baiti norāda izmēru un nākamie 4 baiti norāda veidu). Šeit ir saraksts ar saknes līmeņa atomiem, kas ietverti MP failos:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: satur progresīvu video ielādes/lejupielādes informāciju.
- **moov**: visu filmas metadatu konteiners.
- **moof**: konteiners ar video fragmentiem.
- **mfra**: konteiners ar nejaušu piekļuvi video fragmentam
- **mdat**: datu konteiners multividei.
- **stts**: tabula no parauga līdz laikam.
- **stsc**: tabula no izlases līdz gabalam.
- **stsz**: paraugu izmēri (ierāmēšana)
- **meta**: konteiners ar metadatu informāciju.

Šeit ir MP4 izmantoto otrā līmeņa atomu saraksts:

- **mvhd**: satur video galvenes informāciju ar pilnu informāciju par videoklipu.
- **Trak**: konteiners ar individuālo trasi.
- **udta**: konteiners ar lietotāja un ieraksta informāciju.
- **jodi**: MP4 faila deskriptors

## Atsauces Nr.

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

