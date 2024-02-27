---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD-filformat - Python Dynamic Module
linktitle: PYD
description: Ltjene om PYD filformat og API'er, der kan oprette og åbne PYD fils.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Hvad er en PYD fil?

En PYD-fil er et dynamisk linkbibliotek skrevet i Python, som kan køres af anden Python-kode på kørselstidspunktet. Den indeholder et eller flere Python-moduler, der letter genbrug af kode og giver modularkitektur til at skrive applikationer. PYD-filer kan oprettes og gemmes med filtypenavnet .pyd, f.eks. helloworld.pyd. Applikationsudviklere kan bruge importerklæring til at inkludere PYD-modulerne i deres applikationer. PYD-filer kan åbnes med Python Software Foundation Python, der er tilgængelig til Windows, Mac og Linux OS.

## PYD-filformat - flere oplysninger

PYD-filer er skrevet i Python-programmeringssproget og genereres ved at kompilere Python-koden.

## Forskel mellem PY og PYD filformater

En [PY](/programming/py/)-fil indeholder kildekode, der udføres, som den er, og som ikke kan inkluderes som en genbrugelig kode i andre Python-applikationer. Men en PYD-fil er et dynamisk linket bibliotek, der skal bruges på Windows-operativsystemet.

## Hvordan opretter man PYD-fil?

En PYD-fil kan oprettes ved at oprette et modul med et navn f.eks. exmaple.pyd. Dette modul vil indeholde al funktionaliteten i form af en eller flere funktioner, f.eks. PyMod_example(). Når programmet inkluderer dette bibliotek og kalder det, kan det gøres ved at importere modulet og funktionen PyMod_example() vil køre.

## Referencer ##

 * [Oprettelse af Python-udvidelser i C/C++](https://sebsauvage.net/python/mingw.html)
 * [Python (programmeringssprog) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

