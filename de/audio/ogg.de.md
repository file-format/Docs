---
date: 2019-12-13
keywords: "ogg, ogg-Dateiformat, .ogg-Erweiterung, ogg-Audioformat"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das OGG-Dateiformat und APIs, die OGG-Dateien erstellen und öffnen können."
title: "OGG-Datei - Ogg Vorbis-Audiodatei"
linktitle: "OGG"
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Was ist eine OGG-Datei? ##

OGG ist eine komprimierte Ogg-Vorbis-Audiodatei, die mit der Erweiterung .ogg gespeichert wird. OGG-Dateien werden zum Speichern von Audiodaten verwendet und können auch Künstler- und Titelinformationen sowie Metadaten enthalten. OGG ist ein kostenloses und offenes Containerformat, das von der Xiph.Org Foundation verwaltet wird.

## Kurze Geschichte ##

Das Ogg-Projekt begann 1993 als Teil eines größeren Projekts und hieß Squish, wurde aber aufgrund einer bestehenden Marke in OggSquish umbenannt. Es wurde als Versuch beschrieben, ein flexibles komprimiertes Audioformat für moderne Audioanwendungen zu erstellen. Die OGG-Referenz wurde am 2. September 2000 von Vorbis getrennt.

OGM wurde 2002 aufgrund des Mangels an formeller Videounterstützung in OGG erstellt. Dies ermöglichte das Einbetten von Videos aus dem Microsoft DirectShow-Framework in einen OGG-basierten Wrapper. Bis 2006 wurde OGG von vielen Videospiel-Engines unterstützt und wurde häufig zum Codieren kostenloser Inhalte verwendet. Die Free Software Foundation startete am 15. Mai 2007 eine Kampagne, um die Nutzung von Vorbis als überlegene Alternative zu MP3 zu steigern. Bis zum 30. Juni 2009 war OGG das einzige Containerformat, das von der HTML5-Implementierung von Firefox 3.5 unterstützt wurde.

## OGG-Dateiformat ##

Das OGG-Format besteht aus Datenblöcken. Jeder Chunk wird als Ogg-Seite bezeichnet. Jede Seite beginnt mit „OggS“, um das Ogg-Format zu identifizieren. Die Kopfzeile enthält die fortlaufende Nummer und die Seitennummer, die jede Seite als Teil einer Serie identifiziert. Die Seite besteht aus den folgenden Komponenten.

- **Kopfzeile**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Wert | Beschreibung |
| --- | --- | --- |
| 0 | 0x01 | Gibt an, dass das erste Paket der Seite die Fortsetzung des vorherigen Pakets im logischen Bitstrom ist. |
| 1 | 0x02 | Zeigt an, dass diese Seite die erste im logischen Bitstrom ist. |
| 2 | 0x04 | Zeigt an, dass diese Seite die letzte im logischen Bitstrom ist. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadaten**: VorbisComment ist der am weitesten verbreitete Mechanismus zum Speichern von Metadaten. Andere Mechanismen umfassen die folgenden:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Verweise ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

