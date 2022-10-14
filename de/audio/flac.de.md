---
date: 2019-12-13
keywords: "flac, flac-Dateiformat, .flac-Erweiterung, flac-Datei, flac vs mp3"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das FLAC-Dateiformat und APIs, die FLAC-Dateien erstellen und öffnen können."
title: "FLAC-Dateiformat"
linktitle: "FLAC"
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Was ist eine FLAC-Datei? ##

FLAC (Free Lossless Audio Codec) ist ein von der Xiph.Org Foundation entwickeltes verlustfreies Komprimierungs-Audiocodierungsformat. FLAC ist ein lizenzfreies offenes Format, das mit der Erweiterung .flac gespeichert wird. Mit dem FLAC-Algorithmus komprimiertes digitales Audio wird normalerweise auf 50 bis 70 Prozent in der Größe reduziert. FLAC-Dateien können zu einer identischen Kopie der ursprünglichen Audiodateien dekomprimiert werden.

## FLAC-Dateiformat

Dies ist eine Übersicht über den FLAC-Bitstream.

- **fLaC-Marker**: Dieser Marker wird am Anfang des Streams hinzugefügt. Es folgen ein oder mehrere Metadatenblöcke.
- **Metadatenblöcke**: 128 Arten von Metadatenblöcken werden von FLAC unterstützt; Derzeit sind die folgenden definiert.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Die Audiodaten bestehen aus einem oder mehreren Audioframes.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Kurze Geschichte ##

Josh Coalson begann im Jahr 2000 mit der Entwicklung von FLAC. Die erste Version von FLAC wurde am 20. Juli 2001 veröffentlicht. FLAC wurde am 20. Januar 2003 unter der Xiph.Org-Flagge integriert. Die Entwicklung von FLAC wurde mit in das Xiph.Org-Git-Repository verschoben die Veröffentlichung der Version 1.3.0 am 26. März 2013.

## Zusammensetzung des FLAC-Projekts ##

Das FLAC-Projekt besteht aus Folgendem:

- Stream-Formate.
- Einfaches Containerformat für den Stream (FLAC).
- libFLAC: Eine Bibliothek von Referenz-Encodern, -Decodern und Metadaten-Schnittstellen.
- libFLAC++: Ein objektorientierter Wrapper für libFLAC.
- flac: Ein Befehlszeilenprogramm zum Codieren und Decodieren von FLAC-Streams.
- metaflac: Ein Befehlszeilen-Metadaten-Editor für FLAC.
- Eingabe-Plugins für Musikplayer wie Winamp, XMMX usw.
- Ogg-Containerformat (Ogg FLAC).

## FLAC-Design ##

Je nach Dichte und Amplitude der Musik kann die Größe der komprimierten Datei 80 % kleiner sein als die Originaldatei.

### Quell-Encoder ###

- Es unterstützt nur ganzzahlige Samples und keine Fließkommazahlen. Es kann eine PCM-Bit-Auflösung von 4 bis 32 Bit pro Abtastung und eine Abtastrate von 1 Hz bis 65.535 Hz verarbeiten. Die FLAC-Codierung ist auf 24 Bit pro Sample begrenzt.
- Kanäle können gruppiert werden, um Korrelationen zwischen Kanälen zu nutzen und die Komprimierung zu erhöhen.
- CRC-Prüfsummen werden verwendet, um beschädigte Frames zu identifizieren.
- Für die Konvertierung von Audio-Samples verwendet FLAC die lineare Vorhersage.

### Metadaten ###

- FLAC unterstützt ReplayGain (zur Wahrnehmung und Normalisierung der Lautstärke in Audio).
- FLAC verwendet dasselbe System, das in Vorbis-Kommentaren zum Taggen verwendet wird.
- libFLAC wird von den meisten FLAC-Anwendungen zum Kodieren/Dekodieren verwendet.
- Die libFLAC-API ist in Streams, durchsuchbaren Streams und Dateien organisiert, um die Abstraktion vom Basis-FLAC-Bitstream zu erhöhen.

### Kompression ###

libFLAC verwendet Komprimierungsstufen von 0 bis 8, wobei 0 die schnellste und 8 die langsamste Komprimierungsstufe ist. Die komprimierten Dateien sind immer verlustfrei, obwohl der Kompromiss zwischen Geschwindigkeit und Größe besteht.

## FLAC gegen MP3
MP3 ist ein verlustbehaftetes Komprimierungsformat, was bedeutet, dass ein Teil des Audios abgeschnitten werden kann, um seine Größe nach der Anwendung der Komprimierung zu reduzieren. Dagegen ist FLAC ein verlustfreies Dateiformat, was bedeutet, dass Sie Audio in seiner reinsten Form hören können. Früher waren die verlustfreien Dateiformate CDA oder WAV, die nicht viel platzsparender waren als FLAC. Die folgende Tabelle zeigt den Vergleich zwischen diesen beiden Formaten für einige wichtige Begriffe:

|Term|FLAC|MP3|
---|---|---|
|**Datenqualität**|Kein Verlust von Audiodaten| Beim Komprimieren von Audiodaten können einige Daten verloren gehen|
|**Größe**|Größere Dateigröße im Vergleich zu verlustbehafteten Formaten. Benötigen Sie also eine größere Speicherkapazität | Kleinere Dateigröße, geeignet für die Wiedergabe auf kompakten Audiogeräten mit wenig Speicherplatz |
|**Hardwareanforderungen**| Benötigen Sie hochwertige Audiogeräte und eine riesige Speicherkapazität | Riesige Audiobibliotheken können auf kleinerem Speicherplatz gespeichert werden. Geeignet für Handheld-Geräte wie Audioplayer oder Mobiltelefone|
|**Verteilung über das Internet**|Kann aufgrund der enormen Dateigröße nicht einfach über das Internet verteilt werden |Durch die kompakte Dateigröße ist die Verteilung über das Internet einfach|
|**Kompatibilität**|Der beliebteste Musik- und Audio-Hörcodec, der so ziemlich mit jedem Gerät auf dem Planeten kompatibel ist.Kompatibel mit PCs, Telefonen, AV-Receivern, Blu-ray-Playern und Streaming-Geräten der neuen Generation wie Roku oder Fire TV|

## Verweise ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

