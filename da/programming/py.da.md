---
date: 2019-10-11
keywords: py, python, .py, py file format, how to open py file, how to run py files, how to run python files, how to run python
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY-filformularat
linktitle: PY
description: Ltjene om PY filformat og API'er, der kan oprette og åbne PY fils.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Hvad er PY fil? ##

Filerne med filtypenavnet .py indeholder Python-kildekoden. Python-sproget er blevet et meget berømt sprog nu om dage. Det kan bruges til systemscripting, web- og softwareudvikling og matematik. Python understøtter kompatibilitet på tværs af platforme; betyder, at de udviklede applikationer i Python kan arbejde på forskellige platforme som Windows, MAC, Linux, Raspberry Pi osv. Python giver en enkel og letlæselig syntaks, som ligner det engelske sprog. Udviklere kan skrive en rimelig softwareapplikation ved at skrive et par linjer Python-kode. Da Python kører på et fortolkersystem, så kan koden køres så snart den er skrevet, hvilket gør den meget god til prototyping.

## Kort historie ##

Python was conceived in the late 1980s by Guido van Rossum as a successor to ABC programming language. Its implementation began in December 1989 with Van Rossum as the sole lead developer. He worked on python until 12 July 2018. I januar 2019 valgte de aktive Python-kerneudviklere et Steering Council bestående af fem medlemmer bestående af Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw og Van Rossum til at lede projektet.

### Versioner ###

- Python 2.0 blev udgivet den 16. oktober 2000.
- Python 3.0 blev udgivet den 3. december 2008.

## Sådan kører du py-fil ##

For at kontrollere den installerede version af Python kan du bruge følgende kommando:

```cmd
python --version
```

Dette vil udsende versionen på konsollen som

```cmd
Python 3.7.4
```

Hvis Python ikke er installeret på din maskine, kan du gå til [python.org](https://www.python.org/) og downloade og installere Python til dit relevante operativsystem.

For at udføre et Python-script kan du bruge følgende kommando:

```cmd
python helloworld.py
```

*helloworld.py* er en scriptfil, der indeholder følgende kode

```py
print("Hello World from Python")
```

Dette vil udskrive følgende på konsolvinduet.

```cmd
Hello World from Python
```

Bemærk: Hvis du bruger IDE'er, har de knapper på skærmen eller forskellige tastaturgenveje til at køre Python. For eksempel vises en afspilningsknap i rendestenen med editoren i PyCharm, der lader dig udføre Python-scriptet.

## PY-filformat ##

Python er designet til læsbarhed og har ligheder med engelsk og matematik. Python bruger nye linjer til at angive den komplette kommando i modsætning til semikolon eller parentes brugt på andre sprog. For omfang, loops og funktioner er Python afhængig af indrykning og mellemrum i modsætning til krøllede klammeparenteser, der bruges på andre sprog.

### Syntaks ###

Det følgende er et eksempel på Python-syntaks.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Referencer ##

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

