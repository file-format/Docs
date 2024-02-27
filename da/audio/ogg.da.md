---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om OGG filformat og API'er, der kan oprette og åbne OGG fils.
title: OGG-fil - Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Hvad er OGG fil?

OGG er en Ogg Vorbis-komprimeret lydfil, der er gemt med .ogg-udvidelsen. OGG-filer bruges til lagring af lyddata og kan også omfatte kunstner- og sporoplysninger og metadata. OGG er et gratis og åbent containerformat, der vedligeholdes af Xiph.Org Foundation.

## Kort historie om OGG-filformat

Ogg-projektet startede som en del af et større projekt i 1993 og fik navnet Squish, men på grund af et eksisterende varemærke blev det omdøbt til OggSquish. Det blev beskrevet som et forsøg på at skabe et fleksibelt komprimeret lydformat til moderne lydapplikationer. OGG-reference blev adskilt fra Vorbis den 2. september 2000.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. Den 30. juni 2009 var OGG det eneste containerformat, der blev understøttet af HTML5-implementeringen af Firefox 3.5.

## OGG filformat

OGG-formatet består af bidder af data. Hver del kaldes en Ogg-side. Hver side begynder med OggS for at identificere Ogg-format. Overskriften indeholder serienummeret og sidenummeret, der identificerer hver side som en del af en serie. Siden består af følgende komponenter.

- **Sidehoved**
  - "**Capture Pattern (32 bits)**: Dette bruges til synkronisering ved parsing af OGG-filer."
  - "**Version(8 bit)**: Det angiver versionen af Ogg-bitstrømmen."
  - "**Header Type(8 bits)**: Det angiver sidetypen."

| Bit | Værdi | Beskrivelse |
| --- | --- | --- |
| 0 | 0x01 | Angiver, at den første pakke på siden er fortsættelsen af den forrige pakke i den logiske bitstrøm. |
| 1 | 0x02 | Angiver, at denne side er den første i den logiske bitstrøm. |
| 2 | 0x04 | Indikerer, at denne side er den sidste i den logiske bitstrøm. |

  - "**Granuleposition(64 bit)**: Det er tidsmarkøren, hvis betydning bestemmes af codec'et."
  - "**Bitstream-serienummer(32 bit)**: Det er serienummeret, der identificerer siden, der tilhører en bestemt logisk bitstrøm."
  - "**Sidesekvensnummer(32 bit)**: Det angiver rækkefølgen på siden, hvor den første side starter ved 0."
  - "**Checksum(32 bits)**: Giver CRC32 kontrolsummen for hele sidedata."
  - "**Sidesegmenter(8 bit)**: Angiver antallet af segmenter på siden."
  - "**Segmenttabel**: Det er en matrix af 8-bit værdier, der angiver længden af hvert segment i sideteksten."
- **Metadata**: VorbisComment er den mest udbredte mekanisme til lagring af metadata. Andre mekanismer omfatter følgende:
  - "FLAC-metadatablokke"
  - "Ogg skelet"
  - "Continuous Media Markup Language"

## Referencer ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

