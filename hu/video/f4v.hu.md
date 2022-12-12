---
date: 2019-10-11
keywords: f4v, .f4v, f4v fájlformátum, .f4v fájlformátum, .f4v kiterjesztése, f4v kiterjesztése, f4v videóformátum, az f4v fájlok megnyitása, mik azok az f4v fájlok
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az F4V fájlformátumot és az API-kat, amelyek F4V fájlokat hozhatnak létre és nyithatnak meg"
title: F4V fájlformátum
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Mi az F4V fájl? ##

Az F4V (Flash MP4 Video File) egy .f4v kiterjesztéssel mentett videofájl. Az ISO alap médiafájl-formátumon (MPEG-4, 12. rész) alapul. Nagyon hasonlít az [MP4]-re (/hu/video/mp4/), ezért nem hivatalosan Flash MP4-nek is nevezik. Az [FLV](/hu/video/flv/) korlátozásokkal rendelkezett a H.264/ACC tartalmak streamelése során, ami azt eredményezte, hogy az Adobe Systems létrehozta az új F4V formátumot. A Flash Player a Flash Player 9 3. frissítésének megjelenése óta képes F4V fájlok lejátszására.

## F4V fájlok szerkezete ##

Az F4V fájlformátum az ISO alap médiafájlformátumon (MPEG-4 Part 12) alapul, és nagyon hasonlít az MP4 formátumhoz. A szerkezettel kapcsolatos részletekért lásd az [MP4](/hu/video/mp4/) oldalt. A fő különbség az F4V és az MP4 között az F4V által tárolható metaadatformátumok. Az alábbiakban az F4V formátum által támogatott metaadat-formátumok listája látható.

- **Címkedoboz**: További négy opcionális címkemező (auth, title, dscp, cprt) a Film (moov) mezőben.
- **XMP metaadat doboz**: Ez a mező közvetlenül a Film (moov) mező után található. Ezzel a fájl az ActionScripten keresztül XMP-metaadatokat tud kommunikálni egy SWF-filmmel.
- **ilst box**: Ez a mező a Meta (meta) mezőben található, és számos metaadat címkét tartalmazhat. A támogatott adattípusok alább láthatók.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata box**: Szövegminták (text vagy tx3g) a Media Databoxban (mdat). A következő metaadat-dobozokat tartalmazhatja.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referenciák ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

