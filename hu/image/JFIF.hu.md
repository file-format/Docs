---
date: 2020-08-12
keywords: jfif, .jfif, jfif fájlformátum, jfif fájlok megnyitása, .jfif kiterjesztése, jfif kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF fájl – Mi az a .jfif fájl?
linktitle: JFIF
description: "Ismerje meg a JFIF fájlformátumot és az API-kat, amelyek JFIF fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Mi az a JFIF fájl?

A JFIF (JPEG File Interchange Format (JFIF)) egy képformátumú fájl, amely .jfif kiterjesztést használ. A JFIF a JIF-re (JPEG Interchange Format) épül azáltal, hogy csökkenti a bonyolultságot és megoldja a korlátait.

## A JFIF rövid története

A JFIF-dokumentumfejlesztést Eric Hamilton vezette, és 1991 végén megállapodás született az első verzióról. Az 1.02-es verziót 1992. szeptember 7-én tették közzé. Az RFC 2046 előírja, hogy a JFIF formátumot használják a JPEG képek interneten keresztüli továbbítására. A JFIF-et az ECMA 2009-ben tette közzé, és az ITU-T 2011-ben T.871-es ajánlásaként, az ISO/IEC pedig 2013-ban ISO/IEC 10918-5-ként szabványosította.

## JFIF fájlformátum ##

A JFIF-fájl a JPEG-szabvány 1. részében meghatározott markerek sorozatából áll. Minden marker két bájtból áll (FF, majd egy bájt, amely meghatározza a marker típusát). A jelölők lehetnek önállóak, vagy jelezhetik egy markerszegmens kezdetét.

A JFIF lehetővé teszi, hogy több komponens, például Y, Cb, Cr, eltérő felbontású legyen, de az igazításuk nincs meghatározva. A JPEG-től eltérően a JFIF képes felbontásra és képarányra vonatkozó információkat szolgáltatni. A JFIF meghatározza a használandó színmodellt is.

### Fájlszerkezet ##

|Szegmens|Kód|Leírás|
|---|---|---|
|SOI|FF D8|Kép eleje|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|további marker szegmensek|
|SOS|FF DA|Szkennelés kezdete|
||tömörített képadatok||
|EOI|FF D9|Kép vége|

A JFIF szabvány a következő szegmenseket határozza meg:

### JFIF APP0 markerszegmens ###

Ez egy kötelező képparamétereket tartalmazó szegmens. Beágyazott tömörítetlen bélyegképet is tartalmazhat.

|Mező|Méret (byte)|Leírás|
|---|---|---|
|APP0 marker|2|FF E0|
|Length|2|A szegmens hossza az APP0 marker nélkül|
|Azonosító|5|JFIF (4A 46 49 46 00) az ASCII-ben null byte-tal lezárva|
|JFIF verzió|2|A JFIF verziója|
|Sűrűség mértékegységei|1|A következő pixelsűrűség mezők egysége</br> 00 : Nincs mértékegység; szélesség:magasság pixel képarány megegyezik Ydensity:Xdensity értékkel</br> 01 : Képpont per hüvelyk</br> 02 : Képpont per centiméter|
|Xdensity|2|A vízszintes pixelsűrűség nagyobb, mint nulla|
|Ydensity|2|Függőleges pixelsűrűség nagyobb, mint nulla|
|Xthumbnail|1|A beágyazott RGB-bélyegkép vízszintes pixelszáma. Lehet nulla|
|Ythumbnail|1|A beágyazott RGB-bélyegkép függőleges pixelszáma. Lehet nulla|
|Miniatűr adatok|3 × n|Tömörítetlen 24 bites RGB raszteres miniatűr adatok|

### JFIF bővítmény APP0 markerszegmens ###

Ez egy opcionális szakasz, amely ha definiált, azonnal követnie kell a JFIF APP0 marker szegmenst. Ezt a szakaszt a JFIF 1.02-es és újabb verziója támogatja, és lehetővé teszi miniatűrök beágyazását három különböző formátumban.

|Mező|Méret (byte)|Leírás|
|---|---|---|
|APP0 marker|2|FF E0|
|Length|2|A szegmens hossza az APP0 marker nélkül|
|Azonosító|5|JFXX (4A 46 58 58 00) az ASCII-ben null byte-tal lezárva|
|Miniatűr formátum|1|Meghatározza, hogy milyen adatformátumot használjon a következő beágyazott miniatűr:</br> 10 : JPEG formátum</br> 11 : 1 bájt/pixel palettázott formátum</br> 13 : 3 bájt/pixel RGB formátum|
|Miniatűr adatok|változó||

## JFIF konvertálása más képfájlformátumokká

A JFIF konvertálható népszerű képfájlformátumokká, például [PNG](/hu/image/png/), [JPG](/hu/image/jpeg/) és [PDF](/hu/pdf/).

## Referenciák ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

