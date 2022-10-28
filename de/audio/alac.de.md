---
date: 2021-03-21
keywords: "alac, alac-Dateiformat, .alac-Erweiterung"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Erfahren Sie mehr über das ALAC-Dateiformat und APIs, die ALAC-Dateien erstellen und öffnen können."
title: "ALAC - Apple Lossless Audio Codec-Dateiformat"
linktitle: "ALAC"
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Was ist eine ALAC-Datei? ##

Das ALAC-Dateiformat ist Apple Lossless Audio Codec (ALAC), der den MPEG-4-kompatiblen QuickTime-Container verwendet. Es wurde 2004 als proprietäres Dateiformat eingeführt, bis Apple es 2011 als Open Source und lizenzfrei zur Verfügung stellte. Das Format ähnelt [FLAC](/de/audio/flac/) (Free Lossless Audio Codec), bietet aber vergleichsweise mehr Komprimierung. Es bietet eine besser klingende Alternative zu [AAC](/de/audio/aac/) oder [MP3](/de/audio/mp3/). Mit ALAC-Codec codierte Audiodateien können mit Apple QuickTime, Apple iTunes und Microsoft Windows Media Player mit K-Lite-Codec geöffnet werden.

## ALAC-Dateiformat

Auf dem ALAC-Codec basierende Dateien sind Binärdateien, die als [Open Source auf GitHub](https://github.com/macosforge/alac) als Referenz für Entwickler verfügbar sind. Es enthält die Quellen für den ALAC-Encoder und -Decoder. Apple hat auch ein Befehlszeilenprogramm namens „alacconvert“ bereitgestellt, um die Audiodaten in/aus Core Audio Format (CAF)- und [WAVE](/de/audio/wav/)-Dateien zu lesen und zu schreiben. Im Folgenden finden Sie einige wichtige Punkte zum ALAC-Dateiformat.

1. „Bittiefen“ – 16, 20, 24 und 32 Bit.
1. „Sample Rate“ – Jede beliebige ganzzahlige Abtastrate von 1 bis 384.000 Hz. Theoretische Raten von bis zu 4.294.967.295 (2^32 - 1) Hz könnten unterstützt werden.
1. „Paketgröße“ – Die Standardpaketgröße beträgt standardmäßig 4096 Audio-Sampleframes pro Paket. Andere Paketgrößen sind durchaus möglich. Es kann jedoch nicht garantiert werden, dass nicht standardmäßige Paketgrößen auf allen Hardwaregeräten, die Apple Lossless unterstützen, ordnungsgemäß funktionieren. Pakete über 16.384 Sample-Frames werden nicht unterstützt.
1. „Unterstützte Kanäle“ – Es werden ein bis acht Kanäle unterstützt. Jeder Kanal hat die folgende Informationsreihenfolge.

|Num Chan| Bestellen|
|---|---|
|1 |Mono|
|2 |stereo (links, rechts)|
|3 |MPEG 3.0 B (Mitte, Links, Rechts)|
|4 |MPEG 4.0 B (Mitte, Links, Rechts, Center-Surround)|
|5 |MPEG 5.0 D (Mitte, links, rechts, linker Surround, rechter Surround)|
|6 |MPEG 5.1 D (Mitte, links, rechts, linker Surround, rechter Surround, Niederfrequenzeffekte)|
|7 |Apple AAC 6.1 (Center, Left, Right, Left Surround, Right Surround, Center Surround, Low Frequency Effects)|
|8 |MPEG 7.1 B (Mitte, Mitte links, Mitte rechts, Links, Rechts, Surround links, Surround rechts, Niederfrequenzeffekte)|

## Verweise

* [ALAC – Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec] (https://macosforge.github.io/alac/)
* [macosforge - alac auf GitHub](https://github.com/macosforge/alac)

