---
date: 2019-12-13
keywords: ogg, ogg-filformat, .ogg-tillägg, ogg-ljudformat
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om OGG-filformat och API:er som kan skapa och öppna OGG-filer." 
title: OGG-fil - Ogg Vorbis-ljudfil
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Vad är OGG fil?

OGG är en Ogg Vorbis-komprimerad ljudfil som sparas med tillägget .ogg. OGG-filer används för att lagra ljuddata och kan även innehålla artist- och spårinformation och metadata. OGG är ett gratis och öppet containerformat som underhålls av Xiph.Org Foundation.

## Kort historik om OGG-filformat

Ogg-projektet startade som en del av ett större projekt 1993 och fick namnet Squish men på grund av ett befintligt varumärke döptes det om till OggSquish. Det beskrevs som ett försök att skapa ett flexibelt komprimerat ljudformat för moderna ljudapplikationer. OGG-referensen separerades från Vorbis den 2 september 2000.

OGM skapades 2002 på grund av bristen på formellt videostöd i OGG. Detta gjorde det möjligt att bädda in video från Microsoft DirectShow-ramverket i ett OGG-baserat omslag. År 2006 stöddes OGG av många videospelsmotorer och användes ofta för att koda gratis innehåll. Free Software Foundation startade en kampanj den 15 maj 2007 för att öka användningen av Vorbis som ett överlägset alternativ till MP3. Den 30 juni 2009 var OGG det enda behållarformatet som stöddes av HTML5-implementeringen av Firefox 3.5.

## OGG filformat

OGG-formatet består av bitar av data. Varje bit kallas en Ogg-sida. Varje sida börjar med "OggS" för att identifiera Ogg-format. Rubriken innehåller serienumret och sidnumret som identifierar varje sida som en del av en serie. Sidan består av följande komponenter.

- **Sidhuvud**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Värde | Beskrivning |
| --- | --- | --- |
| 0 | 0x01 | Indikerar att det första paketet på sidan är fortsättningen på det föregående paketet i den logiska bitströmmen. |
| 1 | 0x02 | Indikerar att denna sida är den första i den logiska bitströmmen. |
| 2 | 0x04 | Indikerar att denna sida är den sista i den logiska bitströmmen. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadata**: VorbisComment är den mest stödda mekanismen för att lagra metadata. Andra mekanismer inkluderar följande:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referenser ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

