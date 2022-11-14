---
date: 2020-08-12
keywords: jxr, .jxr, jxr-bestandsindeling, hoe jxr-bestanden te openen, .jxr-extensie, jxr-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR-bestandsindeling
linktitle: JXR
description: "Meer informatie over JXR-bestandsindelingen en API's die JXR-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Wat is een JXR-bestand? ##

JPEG XR (JPEG extended range) is een bestandsformaat voor fotografische beelden met continue toon. Het is een compressiestandaard voor stilstaande beelden die is gebaseerd op HD Photo, ontwikkeld door Microsoft. Het ondersteunt zowel lossy als lossless compressie.

## Korte geschiedenis ##

Windows Media Photo werd voor het eerst aangekondigd door Microsoft op WinHEC 2006. Het werd in november 2006 omgedoopt tot HD Photo. JPEG XR werd op 19 juni 2009 goedgekeurd als internationale standaard ISO/IEC 29199-2. De ITU-T en ISO/IEC publiceerden een motie formaatspecificatie (ITU-T T.833 | ISO/IEC 29199-3), een conformiteitstestset (ITU-T T.834 | ISO/IEC 29199-4) en referentiesoftware (ITU-T T.835 | ISO /IEC 29199-5) voor JPEG XR na voltooiing van de beeldcoderingsspecificatie in 2010. In 2011 werd een technisch rapport gepubliceerd waarin de workflow-architectuur voor JPEG XR werd beschreven.

## JPEG XR-ontwerp ##

In vergelijking met JPEG biedt JPEG XR verschillende verbeteringen, waaronder:

- **Betere compressie**: JPEG XR biedt hogere compressieverhoudingen.
- **Lossless Compression**: JPEG XR ondersteunt lossless compressie.
- **Tegelstructuur**: JPEG XR-afbeelding kan worden gesegmenteerd in tegelgebieden waar elk gebied afzonderlijk kan worden gedecodeerd.
- **Meer kleurnauwkeurigheid**: JPEG XR bevat interne conversie naar de YCoCg-kleurruimte voor ondersteuning van afbeeldingen met RGB-kleurruimte. JPEG XR ondersteunt ook een 16-bits per component (64-bits per pixel) geheel CMYK-kleurmodel. JPEG XR ondersteunt RGBE gedeeld-exponent floating point kleurformaat voor HDR-afbeeldingen. JPEG XR ondersteunt ook grijswaarden en meerkanaals kleurcoderingen.
- **Transparantiekaart**: JPEG XR ondersteunt het alfakanaal voor transparantie.
- **Aanpassing van afbeelding in gecomprimeerd domein**: JPEG XR-afbeeldingen kunnen worden geconverteerd naar codering met verlies, de resolutie wordt verlaagd, bijgesneden, omgedraaid, geroteerd en de tegelstructuur kan worden gewijzigd zonder volledige decodering van het bestand.
- **Metadata-ondersteuning**: JPEG XR-beeldbestand kan ICC-kleurprofiel bevatten voor consistente kleurweergave op meerdere apparaten. Het formaat ondersteunt ook Exif- en XMP-metadataformaten.

## Containerformaat ##

JPEG XR-beeldgegevens kunnen worden opgeslagen in TIFF-achtige containerindeling met behulp van een tabel met IFT-tags (Image File Directory). Een JXR-bestand bevat het volgende in IFD-tags:

- Afbeeldingsgegevens: het zijn aaneengesloten op zichzelf staande afbeeldingsgegevens.
- Optionele alfakanaalgegevens: als deze aanwezig zijn, kunnen de afbeeldingsgegevens afzonderlijk worden gecomprimeerd, zodat toepassingen die geen transparantie ondersteunen, kunnen worden ondersteund.
- Metagegevens
- Optionele XMP-metadata
- Optionele Exif-metadata

Omdat het is gebaseerd op het TIFF-formaat, erft het alle beperkingen van het TIFF-formaat, zoals de maximale bestandsgrootte van 4 GB.

## Referenties ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

