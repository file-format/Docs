---
date: 2019-10-11
keywords: MP4, fájl, kiterjesztés, formátum, videó formátum, MPEG-4
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az MP4 fájlformátumot és az API-kat, amelyek MP4 fájlokat hozhatnak létre és nyithatnak meg."
title: MP4 fájl formátum
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Mi az MP4 fájl? ##

Az MP4 (az MPEG-4 Part 14 rövidítése) egy ISO/IEC 14496-12:2004 szabványon alapuló fájlformátum, amely a QuickTime fájlformátumon alapul, de formálisan támogatja az Initial Object Descriptor (IOD) és egyéb MPEG-szolgáltatásokat. Leginkább videó és hang tárolására szolgál, de használható feliratok és állóképek tárolására is. Az MP4 fájlok tárolása .mp4 kiterjesztéssel történik. Az MP4 egy nemzetközi audiovizuális kódolási szabvány. A legtöbb modern konténerformátumhoz hasonlóan az MP4 is támogatja az interneten keresztüli streamelést. Az MP4-ben használt magas tömörítés miatt az eredményül kapott fájlok kisebbek, és szinte az összes eredeti minőség megmarad.

## Rövid története ##

Az MP4 specifikációt a Moving Picture Experts Group (MPEG) fejlesztette ki, és a QuickTime formátumon [MOV](/hu/video/mov/) alapult, amelyet 2001-ben tettek közzé. Az MP4 első verziója (ISO/IEC 14496-1:2001) az MPEG-4 1. rész: Rendszerspecifikáció 1999-ben közzétett változata volt. Az MP4 fájlformátumot az ISO Base Media File Format ISO/IEC 14496-12:2004 szabványra általánosították, amely meghatározta az időalapú médiafájlok általános szerkezetét. Ennek eredményeként más fájlformátumok alapjául szolgál.

## MP4 fájlok szerkezete ##

Az MP4 egy bővíthető tárolófájl, ami azt jelenti, hogy nem határoz meg szigorú struktúrát, és egyéni struktúrát és hierarchiát tesz lehetővé minden médiatípushoz. Az MP4 fájl adatai két részre oszlanak, az első a médiával kapcsolatos adatokat, a második pedig a metaadatokat tartalmazza. A médiaadatok hangot vagy videót tartalmaznak, a metaadatok pedig véletlenszerű hozzáférést, időbélyegeket stb.
Az MP4 struktúráit általában atomoknak vagy dobozoknak nevezik. Egy atom minimális mérete 8 bájt (az első 4 bájt a méretet, a következő 4 bájt pedig a típust határozza meg). Íme az MP-fájlok gyökérszintű atomjainak listája:

- **ftyp**: A fájl típusát, leírását és a használt általános adatstruktúrákat tartalmazza.
- **pdin**: Progresszív videóbetöltési/letöltési információkat tartalmaz.
- **moov**: Tároló a film összes metaadatához.
- **moof**: tároló videorészletekkel.
- **mfra**: A tároló véletlenszerű hozzáféréssel a videórészlethez
- **mdat**: Adattároló adathordozóhoz.
- **stts**: minta-idő táblázat.
- **stsc**: minta-darab táblázat.
- **stsz**: mintaméretek (keretezés)
- **meta**: A metaadat-információkat tartalmazó tároló.

Íme az MP4-ben használt második szintű atomok listája:

- **mvhd**: A videó fejléce-információit tartalmazza a videó teljes részletével.
- **trak**: konténer az egyéni pályával.
- **udta**: A tároló a felhasználó és a pálya adataival.
- **iods**: MP4 fájlleíró

## Referenciák ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

