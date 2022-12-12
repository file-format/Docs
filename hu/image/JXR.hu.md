---
date: 2020-08-12
keywords: jxr, .jxr, jxr fájlformátum, jxr fájlok megnyitása, .jxr kiterjesztése, jxr kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR fájlformátum
linktitle: JXR
description: "Ismerje meg a JXR fájlformátumot és az API-kat, amelyek JXR fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Mi az a JXR fájl? ##

A JPEG XR (JPEG kiterjesztett tartomány) a folyamatos tónusú fényképészeti képek fájlformátuma. Ez egy állókép-tömörítési szabvány, amely a Microsoft által kifejlesztett HD Photo-on alapul. Támogatja a veszteséges és veszteségmentes tömörítést is.

## Rövid története ##

A Windows Media Photo alkalmazást a Microsoft először a WinHEC 2006 alkalmával jelentette be. 2006 novemberében HD Photo névre keresztelték. A JPEG XR-t 2009. június 19-én hagyták jóvá ISO/IEC 29199-2 nemzetközi szabványként. Az ITU-T és az ISO/IEC indítványt tett közzé. formátumspecifikáció (ITU-T T.833 | ISO/IEC 29199-3), megfelelőségi tesztkészlet (ITU-T T.834 | ISO/IEC 29199-4) és referenciaszoftver (ITU-T T.835 | ISO /IEC 29199-5) a JPEG XR-hez a képkódolási specifikáció 2010-es befejezése után. 2011-ben megjelent a JPEG XR munkafolyamat-architektúráját leíró műszaki jelentés.

## JPEG XR Design ##

A JPEG-hez képest a JPEG XR számos fejlesztést kínál, többek között:

- **Jobb tömörítés**: A JPEG XR nagyobb tömörítési arányt kínál.
- **Veszteségmentes tömörítés**: A JPEG XR támogatja a veszteségmentes tömörítést.
- **Csempestruktúra**: A JPEG XR kép csempe régiókra szegmentálható, ahol az egyes régiók külön-külön dekódolhatók.
- **Nagyobb színpontosság**: A JPEG XR belső konverziót tartalmaz YCoCg színtérré, hogy támogassa a képeket RGB színtér használatával. A JPEG XR támogatja a 16 bites komponensenkénti (64 bites képpontonkénti) egész CMYK színmodellt is. A JPEG XR támogatja az RGBE osztott kitevős lebegőpontos színformátumot a HDR képekhez. A JPEG XR támogatja a szürkeárnyalatos és a többcsatornás színkódolást is.
- **Átlátszósági térkép**: A JPEG XR támogatja az alfa-csatornát az átlátszóság érdekében.
- **Tömörített tartományú képmódosítás**: A JPEG XR képek veszteséges kódolásra konvertálhatók, felbontásuk csökkenthető, körbevágható, átfordítható, elforgatható, és a csempe szerkezete módosítható a fájl teljes dekódolása nélkül.
- **Metaadattámogatás**: A JPEG XR képfájl tartalmazhat ICC-színprofilt a több eszköz konzisztens színmegjelenítése érdekében. A formátum támogatja az Exif és XMP metaadat formátumokat is.

## Tárolóformátum ##

A JPEG XR képadatok TIFF-szerű tárolóformátumban tárolhatók az Image File Directory (IFT) címkék táblázatának használatával. A JXR fájl a következőket tartalmazza IFD címkékben:

- Képadatok: Ez egy összefüggő, önálló képadat.
- Opcionális alfa-csatorna adatok: Ha ez megvan, a képadatok külön-külön tömöríthetők, lehetővé téve az átlátszóságot nem támogató alkalmazások támogatását.
- Metaadatok
- Opcionális XMP metaadatok
- Opcionális Exif metaadatok

Mivel TIFF formátumon alapul, örökli a TIFF formátum összes korlátozását, például a 4 GB-os fájlméret korlátozását.

## Referenciák ##

- [JPEG XR - Wikipédia](https://en.wikipedia.org/wiki/JPEG_XR)

