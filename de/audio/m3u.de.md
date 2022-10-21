---
date: 2019-12-13
keywords: "m3u, m3u-Dateiformat, .m3u-Erweiterung, m3u-Multimedia-Wiedergabeliste, m3u-Wiedergabelistenformat"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das M3U-Dateiformat und APIs, die M3U-Dateien erstellen und öffnen können."
title: "M3U-Dateiformat"
linktitle: "M3U"
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Was ist eine M3U-Datei? ##

M3U (MP3-URL) ist eine Audio-Wiedergabelistendatei, die mit der Erweiterung .m3u gespeichert wird. M3U ist keine eigentliche Audiodatei, es verweist nur auf Audio- und manchmal Videodateien. M3U wurde für die Verwendung mit der Winplay3-Software von Fraunhofer entwickelt. Es wird auch von verschiedenen Mediaplayern und Software unterstützt.

## M3U-Dateiformat ##

Es gibt keine offizielle Spezifikation für das M3U-Dateiformat, es ist ein De-facto-Standard. M3U ist eine einfache Textdatei, die die Erweiterung .m3u verwendet, wenn der Text in der Standard-Nicht-Unicode-Codierung des lokalen Systems codiert ist, oder die Erweiterung .m3u8, wenn der Text UTF-8-codiert ist. Jeder Eintrag in der M3U-Datei kann einer der folgenden sein:

- Absoluter Pfad zur Datei
- Dateipfad relativ zur M3U-Datei.
-URL

### Erweitertes M3U ###

Im erweiterten M3U werden zusätzliche Direktiven eingeführt, die mit "#" beginnen und mit einem Doppelpunkt (:) enden, wenn sie Parameter haben. Nachfolgend finden Sie eine Liste von Anweisungen für erweitertes M3U.

- **#EXTM3U** - Dies ist der Dateikopf, der Extended M3U angibt, und muss die erste Zeile der Datei sein.
- **#EXTENC:** - Textcodierung. Es muss die 2. Zeile der Datei sein.
- **#EXTINF:** - Wird für Titelinformationen und andere zusätzliche Eigenschaften verwendet.
- **#PLAYLIST:** - Der Titel der Playlist
- **#EXTGRP:** - Namensgruppierung beginnen
- **#EXTALB:** - Albuminformationen
- **#EXTART:** - Albumkünstler
- **#EXTGENRE** - Albumgenre
- **#EXTM3A** - Einzeldatei-Wiedergabeliste für Albumtitel oder -kapitel.
- **#EXTBYT:** - Dateigröße in Byte.
- **#EXTBIN:** - Es folgen Binärdaten.
- **#EXTIMG:** - Logo, Cover oder andere Bilder.

### HLS M3U ###

HLS (HTTP Live Streaming) wurde von Apple entwickelt, um Audio und Radio auf iOS-Geräte zu streamen. Es basiert auf dem UTF-8-codierten erweiterten M3U. Es wurde 2017 von der IETF als RFC 8216 standardisiert. Die Tags für die HLS-Playlist beginnen mit „#EXT-X-“. Unten finden Sie eine Liste von Tags für HLS

- **EXT-X-VERSION** - Gibt die Kompatibilitätsversion der Datei basierend auf dem Medium und seinem Server an.
- **#EXT-X-START:** - Gibt den bevorzugten Startpunkt für die Wiedergabeliste an.
- **#EXT-X-PLAYLIST-TYPE:** - Gibt den Typ der Wiedergabeliste an (EVENT oder VOD).
- **#EXT-X-TARGETDURATION:** - Gibt die maximale Segmentdauer an.
- **#EXT-X-MEDIA-SEQUENCE:** - Gibt die Mediensequenznummer an.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Zeigt an, dass alle Medienbeispiele unabhängig sind und ohne andere Segmente dekodiert werden können.
- **#EXT-X-MEDIA:** - Es wird verwendet, um Media Playlists zu verknüpfen, die alternative Wiedergaben des gleichen Inhalts enthalten.
- **#EXT-X-STREAM-INF:** - Es gibt einen Variant Stream an, der Teil der Renditions ist.
- **#EXT-X-BYTERANGE:** - Gibt an, dass das Mediensegment ein Teilbereich der Ressource ist, die durch seinen URI identifiziert wird.
- **#EXT-X-DISCONTINUITY** - Zeigt eine Diskontinuität zwischen dem vorangehenden und dem folgenden Mediensegment an.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Ermöglicht die Synchronisierung zwischen verschiedenen Wiedergaben desselben Variant Streams oder verschiedener Variant Streams.
- **#EXT-X-KEY:** - Gibt an, wie Mediensegmente entschlüsselt werden.
- **#EXT-X-MAP:** - Gibt an, wie der Medien-Initialisierungsabschnitt abgerufen wird. Es ist erforderlich, die entsprechenden Mediensegmente zu analysieren.
- **#EXT-X-PROGRAM-DATE-TIME:** - Verknüpft die erste Probe des Mediensegments mit einem absoluten Datum und/oder einer absoluten Uhrzeit.
- **#EXT-X-DATERANGE:** - Es ordnet einen Datenbereich zu.
- **#EXT-XI-FRAMES-ONLY** - Gibt an, dass jedes Mediensegment in der Playlist einen einzelnen I-Frame beschreibt.
- **EXT-XI-FRAME-STREAM-INF** - Zeigt an, dass die Playlist-Datei I-Frames einer Multimedia-Präsentation enthält.
- **#EXT-X-SESSION-DATA:** - Es erlaubt beliebige Sitzungsdaten zu sein
in einer Master-Playlist enthalten.
- **#EXT-X-SESSION-KEY:** - Ermöglicht Verschlüsselungsschlüssel. Der Client kann diese Schlüssel vorab laden, ohne zuerst die Wiedergabeliste zu lesen.
- **#EXT-X-ENDLIST** - Zeigt an, dass der Datei keine weiteren Mediensegmente hinzugefügt werden.

Das Folgende ist die Liste der von M3U verwendeten Internet-Medientypen:

- **application/vnd.apple.mpegurl**: Dies ist der einzige registrierte Medientyp (registriert im Jahr 2009) für M3U, der verwendet wird, um auf die Wiedergabelisten in HLS-Anwendungen zu verweisen.
- Die folgenden Internetmedientypen werden von Nicht-HLS-Anwendungen verwendet.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U-Beispiel ##

Dies ist ein Beispiel für die M3U-Datei.

```console
#EXTM3U
 
#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3
 
#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Verweise ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP-Live-Streaming](https://tools.ietf.org/html/rfc8216)

