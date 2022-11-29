---
date: 2019-10-11
keywords: MP4, fil, filtillägg, format, videoformat, MPEG-4
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om MP4-filformat och API:er som kan skapa och öppna MP4-filer." 
title: MP4 filformat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Vad är en MP4-fil? ##

MP4 (förkortning av MPEG-4 Part 14) är ett filformat baserat på ISO/IEC 14496-12:2004 som är baserat på QuickTime File Format men som formellt anger stöd för Initial Object Descriptors (IOD) och andra MPEG-funktioner. Den används mest för att lagra video och ljud men kan också användas för att lagra undertexter och stillbilder. MP4-filer lagras med tillägget .mp4. MP4 är en internationell audiovisuell kodningsstandard. I likhet med de flesta moderna containerformat stöder MP4 streaming över internet. På grund av den höga komprimeringen som används i MP4 är de resulterande filerna mindre i storlek med nästan all originalkvalitet bevarad.

## Kortfattad bakgrund ##

MP4-specifikationen utvecklades av Moving Picture Experts Group (MPEG) och baserades på QuickTime-formatet [MOV](/sv/video/mov/) som publicerades 2001. Den första versionen (ISO/IEC 14496-1:2001) av MP4 var en revidering av MPEG-4 Del 1: Systemspecifikationen publicerad 1999. MP4-filformatet generaliserades till ISO Base Media File Format ISO/IEC 14496-12:2004 som definierade den allmänna strukturen för tidsbaserade mediafiler. Som ett resultat används den som grund för andra filformat.

## Struktur för MP4-filer ##

MP4 är en förlängningsbar containerfil, vilket innebär att den inte definierar en strikt struktur och tillåter anpassad struktur och hierarki för varje mediatyp. Data i MP4-filen är uppdelad i två sektioner, den första innehåller mediarelaterade data och den andra innehåller metadata. Mediedata innehåller ljud eller video och metadata indikerar flaggor för slumpmässig åtkomst, tidsstämplar, etc.
Strukturerna i MP4 kallas vanligtvis atomer eller lådor. Minsta storlek på en atom är 8 byte (de första 4 byte anger storlek och nästa 4 byte anger typ). Här är en lista över rotnivåatomer som finns i MP-filer:

- **ftyp**: Innehåller filtypen, beskrivningen och de vanliga datastrukturerna som används.
- **pdin**: Innehåller progressiv videoladdnings-/nedladdningsinformation.
- **moov**: Behållare för all filmmetadata.
- **moof**: Behållare med videofragment.
- **mfra**: Behållaren med slumpmässig tillgång till videofragmentet
- **mdat**: Databehållare för media.
- **stts**: exempel-till-tidtabell.
- **stsc**: prov-till-bit-bord.
- **stsz**: provstorlekar (inramning)
- **meta**: Behållaren med metadatainformationen.

Här är en lista över atomer på andra nivån som används i MP4:

- **mvhd**: Innehåller videohuvudinformationen med fullständig information om videon.
- **trak**: Container med det enskilda spåret.
- **udta**: Behållaren med användar- och spårinformation.
- **iods**: MP4-filbeskrivning

## Referenser ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

