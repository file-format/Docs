---
date: 2019-10-11
keywords: WEBM, mi az a WEBM fájl, WEBM fájlformátum
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Ismerje meg a WEBM fájlformátumot és az API-kat, amelyek WEBM-fájlokat hozhatnak létre és nyithatnak meg."
title: WEBM - WebM videofájl formátum
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Mi az a WEBM fájl?

A .webm kiterjesztésű fájl egy nyílt, jogdíjmentes WebM fájlformátumon alapuló videofájl. Videók internetes megosztására tervezték, és meghatározza a fájltároló szerkezetét, beleértve a videó- és hangformátumokat. A WebM 100%-ban ingyenes, és kiváló minőséget valósít meg nyílt technológiákon, például HTML-en, HTTP-n és TCP/IP-n, amelyek bárki számára elérhetőek. A WebM-et kifejezetten a webes videók kiszolgálására tervezték, így alacsony számítási igényű adatfolyam-továbbításra optimalizálták. Ez alkalmassá teszi a videók lejátszására bármilyen eszközön, különösen alacsony fogyasztású netbookokon, kéziszámítógépeken és táblagépeken.

## WEBM fájlformátum

A WebM fájlstruktúra a Matroska [MKV](/hu/video/mkv/) tárolófájl formátum egy részhalmazán alapul. A WebM-fájlokban elérhető videofolyamokat a VP8 vagy VP9 tömörítési technológiával tömörítik, amelyek nagyon hatékonyak a tömörítésben. Hasonlóképpen, a WebM-fájlok hangfolyamait a [Xiph Foundation](https://www.xiph.org/) által kifejlesztett Vorbis vagy Opus kodekekkel tömörítik. Mindezek a videók és audiokodekek jogdíjmentesek, és díjmentesen használhatók.

Az alábbiakban összefoglaljuk a WebM fájlformátum specifikációit.

|Mező|Leírás|
---|---|
|MIME típusú |video/webm|
|Csak hang MIME-típusú |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Videókodek neve| VP8 vagy VP9|
|Audiokodek neve| Vorbis vagy Opus|

### WebM elemek

A WebM, amely a Matroska specifikáció egy részhalmaza, támogatja a Matroska egyes funkcióit. Az alábbiakban a támogatott elemek leírása található.

#### EBML

|Név |Leírás|
---|---|
|EBML|Állítsa be a követendő adatok EBML jellemzőit. Minden EBML dokumentumnak ezzel kell kezdődnie.|
|EBMLVersion |A fájl létrehozásához használt EBML-elemző verziója.|
|EBMLReadVersion|Az a minimális EBML-verzió, amelyet egy elemzőnek támogatnia kell a fájl olvasásához.|
|EBMLMaxIDLength |Az ebben a fájlban található azonosítók maximális hossza (Matroskában legfeljebb 4).|
|EBMLMaxSizeLength|Az ebben a fájlban található méretek maximális hossza (Matroskában legfeljebb 8). Ez nem írja felül az elem elején jelzett elemméretet. Azokat az elemeket, amelyeknek a jelzett mérete nagyobb, mint az EBMLMaxSizeLength által megengedett mérete, érvénytelennek kell tekinteni.|
|DocType|Az EBML fejlécet követő dokumentum típusát leíró karakterlánc (esetünkben "webm").|
|DocTypeVersion|A fájl létrehozásához használt DocType értelmező verziója.|
|DocTypeReadVersion|Az a minimális DocType-verzió, amelyet a tolmácsnak támogatnia kell a fájl olvasásához.|

#### Globális elemek

Jelenleg csak a "Vid" elem támogatott, amely a sérült adatok érvénytelenítésére szolgál, hogy elkerülje a váratlan viselkedést a sérült adatok használatakor. A tartalom el van vetve. Arra is használható, hogy helyet foglaljon egy alelemben későbbi használatra.

#### Szegmens
Ez az elem tartalmazza az összes többi legfelső szintű (1. szintű) elemet. A Matroska fájl általában 1 szegmensből áll.

#### Meta Információkeresés

A következő információkeresés támogatott.

|Elem neve |Leírás|
---|---|
|SeekHead |Egy másik 1. szintű elem pozícióját tartalmazza.|
|Seek |Egyetlen keresési bejegyzést tartalmaz egy EBML elemhez.|
|SeekID |Az elem nevének megfelelő bináris azonosító.|
|SeekPosition |Az elem pozíciója a szegmensben oktettben (0 = első 1. szintű elem).|

## Hivatkozások

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)

