---
date: 2022-05-09
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI fájlformátum – Python interfész definíció
linktitle: PYI
description: "Ismerje meg a PYI fájlformátumot és az API-kat, amelyek PYI fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Mi az a PYI fájl?

A PYI fájl egy Python Interface Definition fájl, amely kódcsonk hivatkozást tartalmaz az interfész megvalósításához. Minden Python-modul .pyi csonkként jelenik meg, amely normál Python-fájl, de üres metódusokkal. A PYI fájlok szintaxisa megegyezik a normál Python moduléval. Az üres metódusok megvalósítása a végfelhasználóra van bízva, hogy elérje azt a konkrét célt, amelyre a modul íródott. Ez az, ahol a PYI fájlok eltérnek a [PY](/hu/programming/py/) fájloktól, amelyek a program teljes megvalósítását tartalmazzák. A PYI fájlok olyan szövegszerkesztőkkel nyithatók meg, mint a Notepad, Notepad++, Microsoft Visual Studio Code és JetBrains PyCharm.

## PYI fájlformátum

A PYI fájlok egyszerű szöveges fájlokként kerülnek mentésre, amelyek bármely szövegszerkesztővel megnyithatók. A Python egy tolmácsnyelv, amely típusellenőrzést végez a kód végrehajtásakor. Ebben az esetben a PYI fájlok előnyösek, mivel a fejlesztők manuálisan határozhatják meg és ellenőrizhetik a modul típusait az alkalmazás írása közben.

## Referenciák ##

* [Interfészek – Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM Interpreters](https://github.com/interpreters/pym)

