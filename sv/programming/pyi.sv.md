---
date: 2022-05-09
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI-filformat - Python-gränssnittsdefinition
linktitle: PYI
description: "Lär dig om PYI-filformat och API:er som kan skapa och öppna PYI-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Vad är PYI fil?

En PYI-fil är en Python Interface Definition-fil som innehåller kodstubreferens för implementering av gränssnittet. Varje Python-modul representeras som en .pyi-stub som är en normal Python-fil men med tomma metoder. Syntaxen för PYI-filer är densamma som för en vanlig Python-modul. Implementeringen av de tomma metoderna lämnas åt slutanvändaren för att uppnå specifika mål som modulen är skriven för. Det är där PYI-filer skiljer sig från [PY](/sv/programming/py/)-filer som innehåller fullständig implementering av programmet. PYI-filer kan öppnas med textredigerare som Notepad, Notepad++, Microsoft Visual Studio Code och JetBrains PyCharm.

## PYI filformat

PYI-filer sparas som vanliga textfiler som kan öppnas med vilken textredigerare som helst. Python är ett tolkspråk som utför typkontroll när koden körs. I sådana fall är PYI-filer fördelaktiga på det sättet att utvecklare manuellt kan definiera och kontrollera en moduls typer medan de skriver applikationen.

## Referenser ##

* [Gränssnitt - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM Tolkar](https://github.com/interpreters/pym)

