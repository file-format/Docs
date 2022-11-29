---
date: 2022-05-09
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD-filformat - Python Dynamic Module
linktitle: PYD
description: "Lär dig om PYD-filformat och API:er som kan skapa och öppna PYD-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Vad är en PYD fil?

En PYD-fil är ett dynamiskt länkbibliotek skrivet i Python som kan köras av annan Python-kod vid körning. Den innehåller en eller flera Python-moduler som underlättar kodåteranvändning och tillhandahåller modularkitektur för att skriva applikationer. PYD-filer kan skapas och sparas med filtillägget .pyd, t.ex. helloworld.pyd. Applikationsutvecklare kan använda importsatsen för att inkludera PYD-modulerna i sina applikationer. PYD-filer kan öppnas med Python Software Foundation Python som är tillgänglig för Windows, Mac och Linux OS.

## PYD-filformat - Mer information

PYD-filer är skrivna i Python-programmeringsspråket och genereras genom att kompilera Python-koden.

## Skillnad mellan PY och PYD filformat

En [PY](/sv/programming/py/)-fil innehåller källkod som körs som den är och kan inte inkluderas som en återanvändbar kod i andra Python-applikationer. En PYD-fil är dock ett dynamiskt länkat bibliotek som ska användas i Windows-operativsystemet.

## Hur man skapar en PYD-fil?

En PYD-fil kan skapas genom att skapa en modul med ett namn t.ex. exmaple.pyd. Denna modul kommer att innehålla all funktionalitet i form av en eller flera funktioner, t.ex. PyMod_example(). När programmet inkluderar detta bibliotek och anropar det kan det göras genom att importera modulen och funktionen PyMod_example() kommer att köras.

## Referenser ##

* [Skapa Python-tillägg i C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

