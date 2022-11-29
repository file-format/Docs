---
date: 2020-08-12
keywords: jxr, .jxr, jxr filformat, hur man öppnar jxr-filer, .jxr extension, jxr extension
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR filformat
linktitle: JXR
description: "Lär dig om JXR-filformat och API:er som kan skapa och öppna JXR-filer." 
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Vad är en JXR fil? ##

JPEG XR (JPEG extended range) är ett filformat för fotografiska bilder med kontinuerliga toner. Det är en komprimeringsstandard för stillbilder som är baserad på HD Photo utvecklad av Microsoft. Den stöder både förlustfri och förlustfri kompression.

## Kortfattad bakgrund ##

Windows Media Photo tillkännagavs först av Microsoft vid WinHEC 2006. Det döptes om till HD Photo i november 2006. JPEG XR godkändes som internationell standard ISO/IEC 29199-2 den 19 juni 2009. ITU-T och ISO/IEC publicerade en motion formatspecifikation (ITU-T T.833 | ISO/IEC 29199-3), en överensstämmelsetestsats (ITU-T T.834 | ISO/IEC 29199-4) och referensprogramvara (ITU-T T.835 | ISO /IEC 29199-5) för JPEG XR efter slutförandet av bildkodningsspecifikationen 2010. En teknisk rapport som beskriver arbetsflödesarkitekturen för JPEG XR publicerades 2011.

## JPEG XR Design ##

Jämfört med JPEG erbjuder JPEG XR flera förbättringar inklusive:

- **Bättre komprimering**: JPEG XR erbjuder högre kompressionsförhållanden.
- **Förlustfri komprimering**: JPEG XR stöder förlustfri komprimering.
- **Brickstruktur**: JPEG XR-bild kan segmenteras i rutområden där varje region kan avkodas separat.
- **Mer färgnoggrannhet**: JPEG XR inkluderar intern konvertering till YCoCg-färgrymden för att stödja bilder med RGB-färgrymd. JPEG XR stöder också en 16-bitars per komponent (64-bitars per pixel) heltals CMYK-färgmodell. JPEG XR stöder RGBE delad exponent flyttal färgformat för HDR-bilder. JPEG XR stöder även gråskale- och flerkanalsfärgkodningar.
- **Transparency Map**: JPEG XR stöder alfakanalen för transparens.
- **Modifiering av komprimerad domänbild**: JPEG XR-bilder kan konverteras till förlustkodning, reduceras i upplösning, beskäras, vändas, roteras och brickstrukturen kan ändras utan fullständig avkodning av filen.
- **Stöd för metadata**: JPEG XR-bildfil kan innehålla ICC-färgprofil för konsekvent färgrepresentation över flera enheter. Formatet stöder även Exif- och XMP-metadataformat.

## Behållarformat ##

JPEG XR-bilddata kan lagras i TIFF-liknande containerformat genom att använda en tabell med Image File Directory (IFT)-taggar. En JXR-fil innehåller följande i IFD-taggar:

- Bilddata: Det är en sammanhängande fristående bilddata.
- Valfri alfakanalsdata: Om detta finns kan bilddata komprimeras separat för att möjliggöra stöd för applikationer som inte stöder transparens.
- Metadata
- Valfri XMP-metadata
- Valfri Exif-metadata

Eftersom det är baserat på TIFF-format, ärver det alla TIFF-formatbegränsningar som 4 GB filstorleksgräns.

## Referenser ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

