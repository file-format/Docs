---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om FLV filformat og API'er, der kan oprette og åbne FLV fils.
title: FLV fil formularat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Hvad er en FLV fil? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe-systemer oprettede F4V i 2007 på grund af begrænsningerne i FLV.

### Indkodning ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. Version 8 af Flash Player-understøttelse af On2 TrueMotion VP6-videobitstreams. Det er det anbefalede komprimeringsformat til Flash Player 8 og nyere. FLV understøtter lyd i MP3, Nellymoser Asao Codec og open source Speex codec. Det understøtter også ukomprimeret lyd eller lyd i ADPCM-format. AAC (HE-AAC/AAC SBR, AAC Main Profile og AAC-LC) understøttes af de seneste versioner af Flash Player 9.

## Struktur ##

FLV-filer består af Header og Packets. En FLV-fil starter med Headeren. Overskriften har følgende felter.

- **Signatur**: Dens værdi er FLV
- **Version**: Its default value is 1. Kun 0x01 er gyldig.
- **Flag**: 0x04 bruges til lyd og 0x01 bruges til video, så 0x05 bruges til både lyd og video.
- **Header Size**: The default value is 9. Den bruges til at springe en nyere udvidet overskrift over.

Efter overskriften kommer Pakkerne. FLV-filen er opdelt i flere pakker kaldet FLV-tags, der har 15-byte headers. Pakkerne indeholder metadata for lyd, video, scripts, krypteringsoplysninger og nyttelast. FLV-pakkerne har følgende felter.

- **Reserveret**: Det er reserveret til FMS og skal være 0.
- **Filter**: Angiver om pakkerne er filtreret eller ej.
  - "**0**: Ingen forbehandling nødvendig. Dette bruges til ukrypterede filer."
  - "**1**: Forbehandling påkrævet. Dette bruges til krypterede filer"
- **Pakketype**: Dette definerer typen af indhold i pakken.
  - "**8**: Lyd"
  - "**9**: Video"
  - "**18**: Scriptdata"
- **Datastørrelse**: Dette angiver længden af meddelelsen.
- **Timestamp Lower**: Dette gemmer tidsstemplet i millisekunder, hvor tagdataene gælder. Den er sat til NULL for den første pakke.
- **Timestamp Upper**: Udvidelse for at skabe en uint32_be-værdi.
- **Stream ID**: Dette er indstillet til NULL for den første stream.
- **Nyttelastdata**: Dette er data baseret på pakketypen.

## Referencer ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

