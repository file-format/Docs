---
date: 2020-08-12
keywords: "jxr, .jxr, jxr-Dateiformat, wie man jxr-Dateien öffnet, .jxr-Erweiterung, jxr-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JXR-Dateiformat"
linktitle: "JXR"
description: "Erfahren Sie mehr über das JXR-Dateiformat und APIs, die JXR-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Was ist eine JXR-Datei? ##

JPEG XR (JPEG Extended Range) ist ein Dateiformat für Halbton-Fotobilder. Es handelt sich um einen Komprimierungsstandard für Standbilder, der auf HD Photo basiert und von Microsoft entwickelt wurde. Es unterstützt sowohl verlustbehaftete als auch verlustfreie Komprimierung.

## Kurze Geschichte ##

Windows Media Photo wurde erstmals von Microsoft auf der WinHEC 2006 angekündigt. Es wurde im November 2006 in HD Photo umbenannt. JPEG XR wurde am 19. Juni 2009 als internationaler Standard ISO/IEC 29199-2 genehmigt. Die ITU-T und ISO/IEC veröffentlichten einen Antrag Formatspezifikation (ITU-T T.833 | ISO/IEC 29199-3), ein Konformitätstestset (ITU-T T.834 | ISO/IEC 29199-4) und Referenzsoftware (ITU-T T.835 | ISO /IEC 29199-5) für JPEG XR nach Abschluss der Bildkodierungsspezifikation im Jahr 2010. Ein technischer Bericht, der die Arbeitsablaufarchitektur für JPEG XR beschreibt, wurde 2011 veröffentlicht.

## JPEG-XR-Design ##

Im Vergleich zu JPEG bietet JPEG XR mehrere Verbesserungen, darunter:

- **Bessere Komprimierung**: JPEG XR bietet höhere Komprimierungsraten.
- **Verlustfreie Komprimierung**: JPEG XR unterstützt verlustfreie Komprimierung.
- **Kachelstruktur**: JPEG-XR-Bilder können in Kachelregionen segmentiert werden, wobei jede Region separat dekodiert werden kann.
- **Mehr Farbgenauigkeit**: JPEG XR enthält eine interne Konvertierung in den YCoCg-Farbraum zur Unterstützung von Bildern mit dem RGB-Farbraum. JPEG XR unterstützt auch ein ganzzahliges CMYK-Farbmodell mit 16 Bit pro Komponente (64 Bit pro Pixel). JPEG XR unterstützt das RGBE-Gleitkomma-Farbformat mit gemeinsamen Exponenten für HDR-Bilder. JPEG XR unterstützt auch Graustufen- und Mehrkanal-Farbcodierungen.
- **Transparenzkarte**: JPEG XR unterstützt den Alphakanal für Transparenz.
- **Modifikation von komprimierten Domain-Bildern**: JPEG-XR-Bilder können in verlustbehaftete Codierung konvertiert, in der Auflösung reduziert, zugeschnitten, gespiegelt, gedreht und die Kachelstruktur geändert werden, ohne dass die Datei vollständig decodiert werden muss.
- **Metadaten-Unterstützung**: Die JPEG-XR-Bilddatei kann ein ICC-Farbprofil für eine konsistente Farbdarstellung auf mehreren Geräten enthalten. Das Format unterstützt auch Exif- und XMP-Metadatenformate.

## Containerformat ##

JPEG-XR-Bilddaten können im TIFF-ähnlichen Containerformat gespeichert werden, indem eine Tabelle mit IFT-Tags (Image File Directory) verwendet wird. Eine JXR-Datei enthält Folgendes in IFD-Tags:

- Bilddaten: Es handelt sich um zusammenhängende, in sich geschlossene Bilddaten.
- Optionale Alphakanaldaten: Wenn diese vorhanden sind, können die Bilddaten separat komprimiert werden, was die Unterstützung von Anwendungen ermöglicht, die keine Transparenz unterstützen.
- Metadaten
- Optionale XMP-Metadaten
- Optionale Exif-Metadaten

Da es auf dem TIFF-Format basiert, erbt es alle Einschränkungen des TIFF-Formats, wie z. B. die Dateigrößenbeschränkung von 4 GB.

## Verweise ##

- [JPEG-XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

