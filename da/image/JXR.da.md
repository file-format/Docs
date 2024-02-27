---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR fil formularat
linktitle: JXR
description: Ltjene om JXR filformat og API'er, der kan oprette og åbne JXR fils.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Hvad er JXR fil? ##

JPEG XR (JPEG extended range) er et filformat til fotografiske billeder med kontinuerlig tone. Det er en komprimeringsstandard for stillbilleder, der er baseret på HD Photo udviklet af Microsoft. Det understøtter både tabsgivende og tabsfri kompression.

## Kort historie ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. Det blev omdøbt til HD Photo i november 2006. JPEG XR blev godkendt som international standard ISO/IEC 29199-2 den 19. juni 2009. ITU-T og ISO/IEC offentliggjorde en bevægelsesformatspecifikation (ITU-T T.833 | ISO/ IEC 29199-3), et overensstemmelsestestsæt (ITU-T T.834 | ISO/IEC 29199-4) og referencesoftware (ITU-T T.835 | ISO/IEC 29199-5) til JPEG XR efter færdiggørelsen af billedkodningsspecifikationen i 2010. En teknisk rapport, der beskriver workflow-arkitekturen for JPEG XR, blev offentliggjort i 2011.

## JPEG XR-design ##

Sammenlignet med JPEG tilbyder JPEG XR adskillige forbedringer, herunder:

- **Bedre komprimering**: JPEG XR tilbyder højere kompressionsforhold.
- **Tabsfri komprimering**: JPEG XR understøtter tabsfri komprimering.
- **Tilstruktur**: JPEG XR-billede kan segmenteres i fliseområder, hvor hver region kan afkodes separat.
- **Større farvenøjagtighed**: JPEG XR inkluderer intern konvertering til YCoCg-farverum for at understøtte billeder ved hjælp af RGB-farverum. JPEG XR understøtter også en 16-bit pr. komponent (64-bit pr. pixel) heltals CMYK-farvemodel. JPEG XR understøtter RGBE shared-exponent floating point-farveformat til HDR-billeder. JPEG XR understøtter også gråtoner og flerkanals farvekodninger.
- **Transparency Map**: JPEG XR understøtter alfakanalen for gennemsigtighed.
- **Billedmodifikation af komprimeret domæne**: JPEG XR-billeder kan konverteres til kodning med tab, reduceres i opløsning, beskæres, vendes, roteres, og flisestrukturen kan ændres uden fuld afkodning af filen.
- **Metadataunderstøttelse**: JPEG XR-billedfil kan indeholde ICC-farveprofil for ensartet farvegengivelse på tværs af flere enheder. Formatet understøtter også Exif- og XMP-metadataformater.

## Containerformat ##

JPEG XR-billeddata kan gemmes i TIFF-lignende containerformat ved at bruge en tabel med Image File Directory-tags (IFT). En JXR-fil indeholder følgende i IFD-tags:

- Billeddata: Det er en sammenhængende selvstændig billeddata.
- Valgfri alfakanaldata: Hvis dette er til stede, kan billeddataene komprimeres separat, hvilket muliggør understøttelse af applikationer, der ikke understøtter gennemsigtighed.
- Metadata
- Valgfri XMP-metadata
- Valgfri Exif-metadata

Da det er baseret på TIFF-format, arver det alle TIFF-formatbegrænsningerne som f.eks. filstørrelsesgrænsen på 4 GB.

## Referencer ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

