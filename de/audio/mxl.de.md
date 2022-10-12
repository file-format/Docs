---
date: 2022-03-20
keywords: "mxl, Musepack-Dateiformat, Erweiterung .mxl"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Erfahren Sie mehr über das MXL-Dateiformat und APIs, die MXL-Dateien erstellen und öffnen können."
title: "MXL-Dateiformat - Komprimierte MusicXML-Datei"
linktitle: "MXL"
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Was ist eine MXL-Datei?

Eine MXL-Datei ist die komprimierte Form des MusicXML-Dateiformats, das ein offenes Standardformat für den Austausch von digitalen Noten ist. Nur-Text-MusicXML-Dateien sind groß und die Verwendung solcher Dateien als Blattverteilungsformat wurde durch die große Dateigröße beeinträchtigt. Dieses Problem wurde mit [MusicXML](https://www.musicxml.com/) 2.0 behandelt, indem das MXL-Dateiformat eingeführt wurde, das die Dateien ausreichend komprimiert, um die Dateigröße ähnlich wie bei Original-MIDI-Dateien zu reduzieren. Der empfohlene Medientyp für MXL-Dateien ist application/vnd.recordare.musicxml.

## MXL-Dateiformat

MXL-Dateien werden als [ZIP](/de/compression/zip/) komprimierte [XML](/de/web/xml/)-Dateien mit der Dateierweiterung .mxl gespeichert. MXL-Dateien werden mit dem DEFLATE-Algorithmus komprimiert, wie in [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt) angegeben.

### MXL-Dateistruktur

Jede MXL-Datei hat ein ZIP-basiertes XML-Format, das eine META-INF/container.xml-Datei haben muss, die den Ausgangspunkt der MusicXML-Version der Datei beschreibt. Für das MXL-Dateiformat ist keine entsprechende .xsd-Datei definiert.

Eine einfache container.xml-Datei hat folgenden Inhalt. Dieses Beispiel stammt aus der Datei Dichterliebe01.mxl, die auf der MakeMusic-Website verfügbar ist.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
In diesem Beispiel ist die<container> element ist das Dokumentelement. Das<rootfiles> Element kann eine oder mehrere enthalten<rootfile> Elemente, mit dem ersten<rootfile> Element, das den MusicXML-Stamm beschreibt. Eine MusicXML-Datei, die als<rootfile> könnte haben<score-partwise> ,<score-timewise> , oder<opus> als Dokumentelement.

## Verweise

* [Komprimierte MXL-Dateien](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

