---
date: 2019-10-11
keywords: "MP4, Datei, Erweiterung, Format, Videoformat, MPEG-4"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das MP4-Dateiformat und APIs, die MP4-Dateien erstellen und öffnen können."
title: "MP4-Dateiformat"
linktitle: "MP4"
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Was ist eine MP4-Datei? ##

MP4 (kurz für MPEG-4 Part 14) ist ein Dateiformat basierend auf ISO/IEC 14496-12:2004, das auf dem QuickTime-Dateiformat basiert, aber formell die Unterstützung für Initial Object Descriptors (IOD) und andere MPEG-Funktionen spezifiziert. Es wird hauptsächlich zum Speichern von Video und Audio verwendet, kann aber auch zum Speichern von Untertiteln und Standbildern verwendet werden. MP4-Dateien werden mit der Erweiterung .mp4 gespeichert. MP4 ist ein internationaler audiovisueller Kodierungsstandard. Ähnlich wie die meisten modernen Containerformate unterstützt MP4 das Streamen über das Internet. Aufgrund der hohen Komprimierung, die in MP4 verwendet wird, sind die resultierenden Dateien kleiner, wobei fast die gesamte Originalqualität erhalten bleibt.

## Kurze Geschichte ##

Die MP4-Spezifikation wurde von der Moving Picture Experts Group (MPEG) entwickelt und basierte auf dem QuickTime-Format [MOV](/de/video/mov/), das 2001 veröffentlicht wurde. Die erste Version (ISO/IEC 14496-1:2001) von MP4 war eine Überarbeitung der MPEG-4 Teil 1: Systemspezifikation, die 1999 veröffentlicht wurde. Das MP4-Dateiformat wurde auf das ISO-Basismediendateiformat ISO/IEC 14496-12:2004 verallgemeinert, das die allgemeine Struktur für zeitbasierte Mediendateien definierte. Daher wird es als Grundlage für andere Dateiformate verwendet.

## Struktur von MP4-Dateien ##

MP4 ist eine erweiterbare Containerdatei, was bedeutet, dass sie keine strenge Struktur definiert und eine benutzerdefinierte Struktur und Hierarchie für jeden Medientyp ermöglicht. Die Daten in der MP4-Datei sind in zwei Abschnitte unterteilt, wobei der erste die medienbezogenen Daten und der zweite die Metadaten enthält. Die Mediendaten enthalten Audio oder Video und Metadaten zeigen Markierungen für wahlfreien Zugriff, Zeitstempel usw. an.
Die Strukturen in MP4 werden typischerweise als Atome oder Boxen bezeichnet. Die Mindestgröße eines Atoms beträgt 8 Bytes (die ersten 4 Bytes geben die Größe und die nächsten 4 Bytes den Typ an). Hier ist eine Liste der Atome der Wurzelebene, die in MP-Dateien enthalten sind:

- **ftyp**: Enthält den Dateityp, die Beschreibung und die verwendeten gemeinsamen Datenstrukturen.
- **pdin**: Enthält Informationen zum progressiven Laden/Herunterladen von Videos.
- **moov**: Container für alle Filmmetadaten.
- **moof**: Container mit Videofragmenten.
- **mfra**: Der Container mit wahlfreiem Zugriff auf das Videofragment
- **mdat**: Datencontainer für Medien.
- **stts**: Sample-to-Time-Tabelle.
- **stsc**: Sample-to-Chunk-Tabelle.
- **stsz**: Beispielgrößen (Rahmen)
- **meta**: Der Container mit den Metadateninformationen.

Hier ist eine Liste von Atomen der zweiten Ebene, die in MP4 verwendet werden:

- **mvhd**: Enthält die Video-Header-Informationen mit allen Details des Videos.
- **trak**: Container mit dem individuellen Track.
- **udta**: Der Container mit den Benutzer- und Trackinformationen.
- **iods**: MP4-Dateideskriptor

## Verweise ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

