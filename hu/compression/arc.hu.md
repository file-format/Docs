---
date: 2019-12-09
keywords: arc, .arc, arc fájlformátum, arc fájlok megnyitása, .arc kiterjesztése, arc kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC fájlformátum
linktitle: ARC
description: "Ismerje meg az ARC fájlformátumot és az API-kat, amelyek ARC-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Mi az ARC fájl?

Az ARC egy veszteségmentes adattömörítési és archiválási formátum, amelyet a System Enhancement Associates (SEA) fejlesztett ki. A fájlformátumot és az azt létrehozó alkalmazást ARC-nek hívják. Az ARC nagyon népszerű volt a betárcsázós BBS korai időszakában, mivel kombinálta a tömörítést és több fájl archiválását ugyanabban a fájlban. Az ARC-t később a [ZIP](/hu/compression/zip/) váltotta fel, amely jobb tömörítési arányt kínált.

Az .arc fájlkiterjesztést számos más, nem kapcsolódó archív fájltípus használja, például az Internet Archívum által több webes erőforrás tárolására használt ARC formátum, a FreeArc archiváló által használt eltérő ARC formátum, a Nintendo által erőforrásokhoz használt eltérő formátum stb. .

## Az ARC fájlformátum rövid története

Az ARC programot Thom Henderson, a System Enhancement Associates-től írta 1985-ben. Ez a program egyetlen archív fájlba csoportosította a fájlokat, és tömörítette is őket. Az ARC program által generált fájlok az .arc kiterjesztést használták. A SEA 1986-ban adta ki az ARC forráskódját, az ARC-t pedig 1987-ben Howard Chu portolta Unixra és Atari ST-re.

Phil Katz a fájlok archiválására és kibontására fejlesztette ki a PKARC-ot és a PKXARC-t. A fájlok ARC fájlformátummal működtek, és lényegesen gyorsabbak voltak. Az ARC-vel ellentétben a Katz a tömörítési és archiválási funkciókat két különböző fájl között osztotta fel, ami csökkentette a futtatásukhoz szükséges memóriaigényt.

A SEA és a Katz közötti per után a SEA kivonult a shareware piacról, és kifejlesztette az ARC+Plus-t teljes képernyős felhasználói felülettel. Az ARC formátum már nem általános PC-n.

## ARC fájlformátum

Az ARC fájl egy fájlfejlécből és fájlból áll, amelyet az archívum vége jelölő követ az alábbiak szerint.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC fájl fejléce ###

|Eltolás|Címke|Típus|Érték|Leírás|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Módszer|
|02|ARCFNT|DS|12|fájlnév|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Tömörített méret|
|13|ARCDAT|DW|0000|Fájl dátuma (MSDOS)|
|15|ARCTIM|DW|0000|Fájlidő (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Tömörítetlen méret|
|1D|ARCFIL|DS|ARCNSZ| |

### Tömörítési módszerek ###

A tömörítési módszer bájtja a használt tömörítési módszert jelzi. Az alábbiakban bemutatjuk az ARC fájlhoz használt tömörítési módszereket.

|Módszer|Név|Leírás|
|---|---|---|
|0|Tárolt|Nem használt tömörítés|
|1|Csomagolt|Ismétlődő futáshosszúságú kódolás (RLE)|
|2|Squeezed|Huffman-kódolás|
|3|Crunched|LZW 4K pufferrel, 12 bites kódok|
|4|Crunched|Először csomagolás, majd LZW 4K puffer 12 bittel|
|5|Crunched|Csomagolás, LZW, 4K puffer, változó hosszúságú (9-12 bit)|
|6|Squashed|LZW, 8K puffer, változó hosszúságú (9-13 bit)|
|7|Crushed|Csomagolás, majd LZW 8K puffer, 2-13 bit (PAK 1.0)|
|8|Distill|Dynamic Huffman 8K pufferrel (PAK 2.0)|

## Hivatkozások

- [ARC (fájlformátum) - Wikipédia](https://en.wikipedia.org/wiki/ARC_(file_format))

