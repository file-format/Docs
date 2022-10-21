---
date: 2019-10-11
keywords: "f4v, .f4v, f4v-Dateiformat, .f4v-Dateiformat, .f4v-Erweiterung, f4v-Erweiterung, f4v-Videoformat, wie man f4v-Dateien öffnet, was sind f4v-Dateien"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das F4V-Dateiformat und APIs, die F4V-Dateien erstellen und öffnen können"
title: "F4V-Dateiformat"
linktitle: "F4V"
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Was ist eine F4V-Datei? ##

F4V (Flash MP4 Video File) ist eine Videodatei, die mit der Erweiterung .f4v gespeichert wird. Es basiert auf dem ISO-Basismediendateiformat (MPEG-4 Part 12). Es ist [MP4](/de/video/mp4/) sehr ähnlich, weshalb es informell auch als Flash MP4 bezeichnet wird. [FLV](/de/video/flv/) hatte Einschränkungen beim Streamen von H.264/ACC-Inhalten, was dazu führte, dass Adobe Systems das neue F4V-Format erstellte. Flash Player kann seit der Veröffentlichung von Flash Player 9 Update 3 F4V-Dateien wiedergeben.

## Struktur von F4V-Dateien ##

Das F4V-Dateiformat basiert auf dem ISO-Basismediendateiformat (MPEG-4 Teil 12) und ist dem MP4-Format sehr ähnlich. Einzelheiten zur Struktur finden Sie auf der Seite [MP4](/de/video/mp4/). Der Hauptunterschied zwischen F4V und MP4 sind die Metadatenformate, die F4V speichern kann. Nachfolgend finden Sie eine Liste der vom F4V-Format unterstützten Metadatenformate.

- **Tag-Box**: Zusätzliche vier optionale Tag-Boxen (auth, title, dscp, cprt) innerhalb der Movie (moov)-Box.
- **XMP-Metadaten-Box**: Diese Box kommt direkt nach der Movie (moov)-Box. Damit kann die Datei XMP-Metadaten über ActionScript an einen SWF-Film übermitteln.
- **ilst-Box**: Diese Box befindet sich innerhalb der Meta-Box (Meta) und kann eine Reihe von Metadaten-Tags enthalten. Die unterstützten Datentypen sind unten angegeben.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata box**: Die Textbeispiele (text oder tx3g) in der Media Databox (mdat). Es kann die folgenden Metadatenfelder enthalten.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Verweise ##

- [Flash-Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

