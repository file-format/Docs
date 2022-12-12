---
date: 2022-05-09
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD fájlformátum - Python dinamikus modul
linktitle: PYD
description: "Ismerje meg a PYD fájlformátumot és az API-kat, amelyek PYD fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Mi az a PYD fájl?

A PYD-fájl egy Pythonban írt dinamikus hivatkozási könyvtár, amelyet futás közben más Python-kód is futtathat. Egy vagy több Python-modult tartalmaz, amelyek megkönnyítik a kód újrafelhasználását, és modularchitektúrát biztosítanak az alkalmazások írásához. A PYD fájlok .pyd kiterjesztéssel hozhatók létre és menthetők, pl. helloworld.pyd. Az alkalmazásfejlesztők az importálási utasítás segítségével beépíthetik a PYD-modulokat alkalmazásaikba. A PYD fájlok a Python Software Foundation Python programmal nyithatók meg, amely Windows, Mac és Linux operációs rendszerhez érhető el.

## PYD fájlformátum - További információ

A PYD fájlok Python programozási nyelven íródnak, és a Python kód fordításával jönnek létre.

## A PY és a PYD fájlformátumok közötti különbség

A [PY](/hu/programming/py/) fájl olyan forráskódot tartalmaz, amely úgy fut le, ahogy van, és nem szerepelhet újrafelhasználható kódként más Python-alkalmazásokban. A PYD-fájlok azonban egy dinamikusan összekapcsolt könyvtár, amelyet a Windows operációs rendszeren kell használni.

## Hogyan lehet PYD fájlt létrehozni?

PYD fájlt úgy lehet létrehozni, hogy pl. exmaple.pyd nevű modult hozunk létre. Ez a modul tartalmazza az összes funkciót egy vagy több függvény formájában, pl. PyMod_example(). Ha a program tartalmazza ezt a könyvtárat, és meghívja, akkor ez megtehető a modul importálásával, és a PyMod_example() függvény fut.

## Referenciák ##

* [Python-kiterjesztések létrehozása C/C++ nyelven](https://sebsauvage.net/python/mingw.html)
* [Python (programozási nyelv) – Wikipédia](https://en.wikipedia.org/wiki/Python_(programozási_nyelv))

