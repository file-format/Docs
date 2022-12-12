---
date: 2019-12-09
keywords: arj, .arj, arj fájlformátum, arj fájlok megnyitása, .arj kiterjesztése, arj kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ fájlformátum
linktitle: ARJ
description: "Ismerje meg az ARJ fájlformátumot és az API-kat, amelyek ARJ-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Mi az ARJ fájl? ##

Az ARJ (Archiválta Robert Jung) egy nagy hatékonyságú tömörített archív fájl, amelyet Robert K. Jung fejlesztett ki. Az ARJ-t DOS-hoz és a Windows korai verzióihoz fejlesztették ki az 1990-es évek elején. Az ARJ-fájlok nagyszámú fájl biztonsági mentéséhez vagy megosztásához hasznosak, mivel nem kell az összes fájlt nyomon követnie, és csak egyetlen fájlt kell kezelni. Az .arj kiterjesztést az ARJ archív fájlok használják.

## ARJ fájlformátum ##

Egy ARJ-fájl kétféle fejlécet tartalmaz:

- Fő fejléc: Az archívum elején egy fő fejléc található.
- Helyi fejlécek: A helyi fejlécek minden fájl előtt jelen vannak.

|Eltolás|Típus|Szám|Leírás|
|---|---|---|---|
|0000h|szó|1|ID=0EA60h|
|0002h|szó|1|alapfejlécméret|
|0004h|byte|1|A fejléc mérete|
|0005h|byte|1|Archiváló verziószáma|
|0006h|byte|1|Minimális verziószám szükséges|
|0007h|byte|1|Gazdagép operációs rendszer:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 – MAC-OS (System xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - NEXT</br> 9 - VAX VMS|
|0008h|byte|1|Belső zászlók, bitképes:</br> 0 - nincs jelszó / jelszó</br> 1 - fenntartva</br> 2 - a fájl a következő lemezen folytatódik</br> 3 - a fájl kezdőpozíciója mező elérhető</br> 4 útvonalú fordítás ( "\" - "/" )|
|0009h|byte|1|Tömörítési módszer:</br> 0 - tárolva</br> 1 - tömörített leginkább</br> 2 - tömörített</br> 3 - gyorsabban tömörített</br> 4 - tömörített leggyorsabban|
|000Ah|byte|1|Fájltípus:</br> 0 - bináris</br> 1-7 bites szöveg</br> 2 - megjegyzés fejléc</br> 3 - könyvtár</br> 4 - kötetcímke|
|000Bh|byte|1|fenntartott|
|000Ch|dword|1|Az eredeti fájl dátuma/ideje MS-DOS formátumban|
|0010h|dword|1|A tömörített fájl mérete|
|0014h|dword|1|Az eredeti fájl mérete"|
|0018h|dword|1|CRC-32 az eredeti fájl|
|001Ah|word|1|Fájlspecifikációs pozíció a fájlnévben|
|001Ch|word|1|Fájlattribútumok|
|001Eh|word|1|Host adatok|
|?|dword|1|Bővített fájl kezdőpozíciója|
|????h|dword|1|az alapfejléc CRC-32|
|????h|word|1|Az első kiterjesztett fejléc mérete|
|????h+"SIZ"+2|dword|1|CRC-32 a kiterjesztett fejlécből|
|????h+"SIZ"+6|byte|?|Tömörített fájl|

## Hivatkozások ##

- [ARJ - Wikipédia](https://en.wikipedia.org/wiki/ARJ)

