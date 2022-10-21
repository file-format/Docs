---
date: 2019-10-11
keywords: "rm, .rm, rm-Dateiformat, .rm-Dateiformat, .rm-Erweiterung, RealMedia-Dateiformat"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das RM-Dateiformat und APIs, die RM-Dateien erstellen und öffnen können."
title: "RM-Dateiformat"
linktitle: "RM"
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Was ist eine RM-Datei? ##

RealMedia ist ein proprietäres Multimedia-Containerformat, das von RealNetworks entwickelt wurde und die Erweiterung .rm verwendet. Es wird mit der Kombination von [RealAudio (RA)](/de/audio/ra/) und [RealVideo(RV)](/de/video/rv/) zum Streamen über das Internet verwendet. Diese Streams haben eine konstante Bitrate. Für variable Bitraten hat RealNetworks das Format RealMedia Variable Bitrate (RMVB) entwickelt. RealMedia eignet sich zum Streamen von Inhalten über das Internet und kann beispielsweise zum Streamen von Live-Fernsehen verwendet werden.

## Struktur der RealMedia-Datei ##

Eine RealMedia-Datei besteht aus einer Reihe von Chunks, die jeweils die folgende Struktur haben:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Die folgenden Chunk-Typen sind in der RealMedia-Datei vorhanden:

- **Header der RealMedia-Datei (.RMF)**: Dies muss der erste Chunk in der RealMedia-Datei sein. In einer Datei ist nur ein RMF-Chunk vorhanden. Es enthält Informationen über die Anzahl der Header.
- **Dateieigenschaften-Header (PROP)**: Dieser enthält Informationen über die allgemeinen Eigenschaften der RealMedia-Datei. In jeder RealMedia-Datei gibt es nur einen Chunk dieses Typs.
- **Media Properties Header (MDPR)**: Dieser Chunk enthält Informationen zu den Stream-Eigenschaften. Es enthält Informationen über die Art des Streams und den verwendeten Codec. Es gibt einen MDPR-Block für jeden Stream in der Datei.
- **Content Description Header (CONT)**: Dieser Chunk enthält Textinformationen wie Titel oder Autor für den Inhalt in der RealMedia-Datei. Dieser Chunk dient nur zu Informationszwecken.
- **Data Header (DATA)**: Dieser Chunk enthält eine Gruppe von Datenpaketen.
- **Index-Header (INDX)**: Dieser Chunk kommt nach allen DATA-Chunks und enthält Indexeinträge. Eine Datei kann mehr als einen INDX-Chunk haben.

## Unterstützte Audio- und Videoformate ##

### Audioformate ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
-sipr: Sipro
- kochen: kochen
- atrc: ATRAC3
- ralf: RealAudio Lossless-Format
- raac: LC-AAC
- Rack: HE-AAC

### Videoformate ###

-CLV1: ClearVideo
-RV10: H.263
-RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264-Vorläufer
- RV40: H.264-Vorläufer, RV40
- RVTR: H.263+ (RV20)

## Verweise ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

