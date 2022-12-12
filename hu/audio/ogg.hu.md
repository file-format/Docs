---
date: 2019-12-13
keywords: ogg, ogg fájlformátum, .ogg kiterjesztés, ogg hangformátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az OGG fájlformátumot és az API-kat, amelyek OGG fájlokat hozhatnak létre és nyithatnak meg."
title: OGG fájl - Ogg Vorbis hangfájl
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Mi az OGG fájl?

Az OGG egy Ogg Vorbis tömörített hangfájl, amely .ogg kiterjesztéssel kerül mentésre. Az OGG fájlokat hangadatok tárolására használják, és tartalmazhatnak előadó- és számadatokat és metaadatokat is. Az OGG egy ingyenes és nyílt konténerformátum, amelyet a Xiph.Org Foundation tart fenn.

## Az OGG fájlformátum rövid története

Az Ogg projekt egy nagyobb projekt részeként indult 1993-ban, és a Squish nevet kapta, de egy meglévő védjegy miatt átnevezték OggSquish-re. Úgy írták le, mint kísérletet egy rugalmas tömörített hangformátum létrehozására a modern audioalkalmazásokhoz. Az OGG referenciát 2000. szeptember 2-án választották el a Vorbistól.

Az OGM-et 2002-ben hozták létre az OGG formális videó támogatásának hiánya miatt. Ez lehetővé tette a Microsoft DirectShow keretrendszerből származó videók beágyazását egy OGG-alapú burkolóba. 2006-ra az OGG-t számos videojáték-motor támogatta, és általában ingyenes tartalmak kódolására használták. A Free Software Foundation 2007. május 15-én kampányt indított a Vorbis, mint az MP3 kiváló alternatívájaként való használatának növelésére. 2009. június 30-án az OGG volt az egyetlen tárolóformátum, amelyet a Firefox 3.5 HTML5 implementációja támogat.

## OGG fájl formátum

Az OGG formátum adatdarabokból áll. Minden egyes darabot Ogg-oldalnak neveznek. Minden oldal "OggS" karakterrel kezdődik az Ogg formátum azonosítására. A fejléc tartalmazza a sorozatszámot és az oldalszámot, amely az egyes oldalakat egy sorozat részeként azonosítja. Az oldal a következő összetevőkből áll.

- **Oldalfej**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Érték | Leírás |
| --- | --- | --- |
| 0 | 0x01 | Azt jelzi, hogy az oldal első csomagja az előző csomag folytatása a logikai bitfolyamban. |
| 1 | 0x02 | Azt jelzi, hogy ez az oldal az első a logikai bitfolyamban. |
| 2 | 0x04 | Azt jelzi, hogy ez az oldal az utolsó a logikai bitfolyamban. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metaadatok**: A VorbisComment a metaadatok tárolásának legszélesebb körben támogatott mechanizmusa. Egyéb mechanizmusok a következők:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Hivatkozások ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

