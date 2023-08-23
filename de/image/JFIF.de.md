---
date: 2020-08-12
keywords: "jfif, .jfif, jfif-Dateiformat, wie man jfif-Dateien öffnet, .jfif-Erweiterung, jfif-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JFIF-Datei - Was ist eine .jfif-Datei?"
linktitle: "JFIF"
description: "Erfahren Sie mehr über das JFIF-Dateiformat und APIs, die JFIF-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Was ist eine JFIF-Datei?

JFIF (JPEG File Interchange Format (JFIF)) ist eine Bildformatdatei mit der Erweiterung .jfif. JFIF baut auf JIF (JPEG Interchange Format) auf, indem es die Komplexität reduziert und seine Einschränkungen beseitigt.

## Kurze Geschichte von JFIF

Die Entwicklung von JFIF-Dokumenten wurde von Eric Hamilton geleitet, und Ende 1991 wurde eine Vereinbarung über die erste Version getroffen. Version 1.02 wurde am 7. September 1992 veröffentlicht. RFC 2046 spezifizierte, dass das JFIF-Format verwendet wird, um JPEG-Bilder über das Internet zu übertragen. JFIF wurde 2009 von der ECMA veröffentlicht und 2011 von der ITU-T als Empfehlung T.871 und 2013 von ISO/IEC als ISO/IEC 10918-5 standardisiert

## JFIF-Dateiformat ##

Eine JFIF-Datei besteht aus einer Folge von Markierungen, wie sie in Teil 1 des JPEG-Standards definiert sind. Jeder Marker besteht aus zwei Bytes (FF gefolgt von einem Byte, das den Typ des Markers angibt). Markierungen können entweder eigenständig sein oder den Beginn eines Markierungssegments anzeigen.

JFIF erlaubt mehreren Komponenten wie Y, Cb, Cr, unterschiedliche Auflösungen zu haben, aber ihre Ausrichtung ist nicht definiert. Im Gegensatz zu JPEG kann JFIF Informationen zur Auflösung und zum Seitenverhältnis bereitstellen. JFIF definiert auch das zu verwendende Farbmodell.

### Dateistruktur ##

|Segment|Code|Beschreibung|
|---|---|---|
|SOI|FF D8|Start des Bildes|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|zusätzliche Markierungssegmente|
|SOS|FF DA|Start des Scans|
||komprimierte Bilddaten||
|EOI|FF D9|Bildende|

Der JFIF-Standard definiert die folgenden Segmente:

### JFIF APP0-Markersegment ###

Es ist ein obligatorisches Segment, das Bildparameter enthält. Es kann auch ein eingebettetes unkomprimiertes Thumbnail enthalten.

|Feld|Größe (Bytes)|Beschreibung|
|---|---|---|
|APP0-Marker|2|FF E0|
|Länge|2|Länge des Segments ohne APP0-Markierung|
|Identifier|5|JFIF (4A 46 49 46 00) in ASCII abgeschlossen durch ein Null-Byte|
|JFIF-Version|2|Version des JFIF|
|Dichteeinheiten|1|Einheit für die folgenden Pixeldichtefelder</br> 00 : Keine Einheiten; Das Pixel-Seitenverhältnis Breite:Höhe entspricht Ydensity:Xdensity</br> 01 : Pixel pro Zoll</br> 02 : Pixel pro Zentimeter|
|Xdensity|2|Horizontale Pixeldichte größer Null|
|Ydensity|2|Vertikale Pixeldichte größer Null|
|Xthumbnail|1|Horizontale Pixelzahl des eingebetteten RGB-Thumbnails. Kann Null sein|
|Ythumbnail|1|Vertikale Pixelzahl des eingebetteten RGB-Thumbnails. Kann Null sein|
|Thumbnail-Daten|3 × n|Unkomprimierte 24-Bit-RGB-Raster-Thumbnail-Daten|

### JFIF-Erweiterung APP0-Markersegment ###

Dies ist ein optionaler Abschnitt, der, falls definiert, unmittelbar auf das JFIF-APP0-Markierungssegment folgen muss. Dieser Abschnitt wird von JFIF Version 1.02 und höher unterstützt und ermöglicht das Einbetten von Miniaturansichten in drei verschiedenen Formaten.

|Feld|Größe (Bytes)|Beschreibung|
|---|---|---|
|APP0-Marker|2|FF E0|
|Länge|2|Länge des Segments ohne APP0-Markierung|
|Bezeichner|5|JFXX (4A 46 58 58 00) in ASCII abgeschlossen durch ein Null-Byte|
|Thumbnail-Format|1|Gibt an, welches Datenformat für das folgende eingebettete Thumbnail verwendet wird:</br> 10 : JPEG-Format</br> 11: 1 Byte pro Pixel, palettiertes Format</br> 13 : 3 Byte pro Pixel RGB-Format|
|Thumbnail-Daten|Variable||

## Konvertierung von JFIF in andere Bilddateiformate

JFIF kann in gängige Bilddateiformate wie [PNG](/de/image/png/), [JPG](/de/image/jpeg/) und [PDF](/de/pdf/) konvertiert werden.

## Verweise ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

