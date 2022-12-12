---
date: 2019-12-13
keywords: m3u, m3u fájlformátum, .m3u kiterjesztésű, m3u multimédiás lejátszási lista, m3u lejátszási lista formátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az M3U fájlformátumot és az API-kat, amelyek M3U fájlokat hozhatnak létre és nyithatnak meg."
title: M3U fájlformátum
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Mi az M3U fájl? ##

Az M3U (MP3 URL) egy .m3u kiterjesztéssel tárolt lejátszási listafájl. Az M3U nem valódi hangfájl, csak hang- és néha videofájlokra mutat. Az M3U-t a Fraunhofer a Winplay3 szoftverrel való használatra fejlesztette ki. Különféle médialejátszók és szoftverek is támogatják.

## M3U fájlformátum

Az M3U fájlformátumra nincs hivatalos specifikáció, ez egy de facto szabvány. Az M3U egy egyszerű szöveges fájl, amely .m3u kiterjesztést használ, ha a szöveg a helyi rendszer alapértelmezett, nem Unicode kódolásával van kódolva, vagy .m3u8 kiterjesztéssel, ha a szöveg UTF-8 kódolású. Az M3U fájl minden bejegyzése a következők egyike lehet:

- A fájl abszolút elérési útja
- Fájl elérési útja az M3U fájlhoz képest.
- URL

### Kiterjesztett M3U ###

A kiterjesztett M3U-ban további direktívák kerülnek bevezetésre, amelyek "#"-val kezdődnek, és kettősponttal (:) végződnek, ha vannak paramétereik. Az alábbiakban a kiterjesztett M3U direktíváinak listája látható.

- **#EXTM3U** - Ez a kiterjesztett M3U-t jelző fájlfejléc, és a fájl első sorának kell lennie.
- **#EXTENC:** - Szövegkódolás. Ennek a fájl 2. sorának kell lennie.
- **#EXTINF:** - A számadatokhoz és egyéb további tulajdonságokhoz használatos.
- **#PLAYLIST:** - A lejátszási lista címe
- **#EXTGRP:** - Kezdje el a névcsoportosítást
- **#EXTALB:** - Album információ
- **#EXTART:** - Album előadója
- **#EXTGENRE** - Album műfaj
- **#EXTM3A** - Egyfájlos lejátszási lista albumszámokhoz vagy fejezetekhez.
- **#EXTBYT:** - Fájlméret bájtban.
- **#EXTBIN:** - Bináris adatok következnek.
- **#EXTIMG:** - Embléma, borító vagy egyéb képek.

### HLS M3U ###

A HLS-t (HTTP Live Streaming) az Apple hozta létre, hogy hangot és rádiót streameljen iOS-eszközökre. Az UTF-8 kódolású kiterjesztett M3U-n alapul. Az IETF 2017-ben RFC 8216 néven szabványosította. A HLS lejátszási lista címkéi „#EXT-X-” karakterekkel kezdődnek. Az alábbiakban a HLS címkéinek listája látható

- **EXT-X-VERSION** - A fájl kompatibilitási verzióját jelzi az adathordozó és a szerver alapján.
- **#EXT-X-START:** - A lejátszási lista kívánt kezdőpontját jelzi.
- **#EXT-X-PLAYLIST-TYPE:** - A lejátszási lista típusát adja meg (EVENT vagy VOD).
- **#EXT-X-TARGETDURATION:** - Meghatározza a szegmens maximális időtartamát.
- **#EXT-X-MEDIA-SEQUENCE:** - A média sorszámát jelzi.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Azt jelzi, hogy minden médiaminta független, és más szegmensek nélkül is dekódolható.
- **#EXT-X-MEDIA:** - Olyan média lejátszási listák összekapcsolására szolgál, amelyek ugyanazon tartalom alternatív megjelenítéseit tartalmazzák.
- **#EXT-X-STREAM-INF:** - Meghatároz egy Változatos adatfolyamot, amely a megjelenítések részét képezi.
- **#EXT-X-BYTERANGE:** - Azt jelzi, hogy a médiaszegmens az URI által azonosított erőforrás egy altartománya.
- **#EXT-X-DISCONTINUITY** - Az előző és a következő médiaszegmensek közötti megszakítást jelzi.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Lehetővé teszi a szinkronizálást ugyanazon Variant Stream vagy különböző Variant Stream különböző megjelenítései között.
- **#EXT-X-KEY:** - Meghatározza a médiaszegmensek visszafejtésének módját.
- **#EXT-X-MAP:** - Meghatározza, hogyan lehet megszerezni az adathordozó inicializálási szakaszt. A vonatkozó médiaszegmensek elemzése szükséges.
- **#EXT-X-PROGRAM-DATE-TIME:** - A médiaszegmens első mintáját abszolút dátumhoz és/vagy időponthoz rendeli.
- **#EXT-X-DATERANGE:** - Adattartományt társít.
- **#EXT-XI-FRAMES-ONLY** - Azt jelzi, hogy a lejátszási listában minden médiaszegmens egyetlen I-kockát ír le.
- **EXT-XI-FRAME-STREAM-INF** - Azt jelzi, hogy a lejátszási lista fájl multimédiás prezentáció I-kockáit tartalmazza.
- **#EXT-X-SESSION-DATA:** - Lehetővé teszi tetszőleges munkamenet adatok létrehozását
fő lejátszási listában.
- **#EXT-X-SESSION-KEY:** - Lehetővé teszi a titkosítási kulcsokat. A kliens előre betöltheti ezeket a kulcsokat anélkül, hogy először elolvasná a lejátszási listát.
- **#EXT-X-ENDLIST** - Azt jelzi, hogy nem lesz több médiaszegmens hozzáadva a fájlhoz.

Az alábbi lista az M3U által használt internetes médiatípusokat tartalmazza:

- **application/vnd.apple.mpegurl**: Ez az egyetlen regisztrált médiatípus (2009-ben regisztrálva) az M3U számára, amelyet a HLS-alkalmazások lejátszási listáira használnak.
- A következő internetes médiatípusokat használják a nem HLS-alkalmazások.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U ## példa

Ez egy példa az M3U fájlra.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Hivatkozások ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP élő közvetítés](https://tools.ietf.org/html/rfc8216)

