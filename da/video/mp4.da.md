---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om MP4 filformat og API'er, der kan oprette og åbne MP4 fils.
title: MP4 fil formularat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Hvad er en MP4-fil? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Kort historie ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. Den første version (ISO/IEC 14496-1:2001) af MP4 var en revision af MPEG-4 Part 1: Systems-specifikationen udgivet i 1999. MP4-filformatet blev generaliseret til ISO Base Media File Format ISO/IEC 14496-12 :2004, der definerede den generelle struktur for tidsbaserede mediefiler. Som følge heraf bruges den som grundlag for andre filformater.

## Struktur af MP4-filer ##

MP4 er en udvidelsesbar containerfil, hvilket betyder, at den ikke definerer en streng struktur og tillader tilpasset struktur og hierarki for hver medietype. Dataene i MP4-filen er opdelt i to sektioner, den første indeholder de medierelaterede data og den anden indeholder metadata. Mediedataene indeholder lyd eller video, og metadata angiver flag for tilfældig adgang, tidsstempler osv.
Strukturerne i MP4 omtales typisk som atomer eller kasser. Minimumsstørrelsen af et atom er 8 bytes (de første 4 bytes angiver størrelse og de næste 4 bytes angiver type). Her er en liste over rodniveauatomer indeholdt i MP-filer:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: Indeholder progressiv videoindlæsning/downloadinformation.
- **moov**: Container til alle filmens metadata.
- **moof**: Container med videofragmenter.
- **mfra**: Beholderen med tilfældig adgang til videofragmentet
- **mdat**: Databeholder til medier.
- **stts**: prøve-til-tidstabel.
- **stsc**: prøve-til-klump bord.
- **stsz**: prøvestørrelser (indramning)
- **meta**: Beholderen med metadataoplysningerne.

Her er en liste over atomer på andet niveau, der bruges i MP4:

- **mvhd**: Indeholder videoheaderoplysningerne med alle detaljer om videoen.
- **trak**: Container med det enkelte spor.
- **udta**: Containeren med bruger- og sporoplysninger.
- **iods**: MP4-filbeskrivelse

## Referencer ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

