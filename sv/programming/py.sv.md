---
date: 2019-10-11
keywords: py, python, .py, py-filformat, hur man öppnar py-fil, hur man kör py-filer, hur man kör python-filer, hur man kör python
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY filformat
linktitle: PY
description: "Lär dig om PY-filformat och API:er som kan skapa och öppna PY-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Vad är PY fil? ##

Filerna med filtillägget .py innehåller källkoden för Python. Python-språket har blivit ett mycket känt språk nu för tiden. Den kan användas för systemskript, webb- och mjukvaruutveckling och matematik. Python stöder plattformsoberoende kompatibilitet; innebär att de utvecklade applikationerna i Python kan fungera på olika plattformar som Windows, MAC, Linux, Raspberry Pi, etc. Python ger en enkel och lättläst syntax som liknar det engelska språket. Utvecklare kan skriva ett rimligt program genom att skriva några rader Python-kod. Eftersom Python körs på ett tolksystem, så kan koden exekveras så fort den är skriven vilket gör den mycket bra för prototyper.

## Kortfattad bakgrund ##

Python skapades i slutet av 1980-talet av Guido van Rossum som en efterträdare till programmeringsspråket ABC. Dess implementering började i december 1989 med Van Rossum som den enda ledande utvecklaren. Han arbetade med python fram till 12 juli 2018. I januari 2019 valde de aktiva Python-kärnutvecklarna en fem-medlems "Steering Council" bestående av Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw och Van Rossum att leda projektet.

### Versioner ###

- Python 2.0 släpptes den 16 oktober 2000.
- Python 3.0 släpptes den 3 december 2008.

## Hur man kör py-fil ##

För att kontrollera vilken version av Python som är installerad kan du använda följande kommando:

```cmd
python --version
```

Detta kommer att mata ut versionen på konsolen som

```cmd
Python 3.7.4
```

Om Python inte är installerat på din maskin kan du gå till [python.org](https://www.python.org/) och ladda ner och installera Python för ditt relevanta operativsystem.

För att köra ett Python-skript kan du använda följande kommando:

```cmd
python helloworld.py
```

*helloworld.py* är en skriptfil som innehåller följande kod

```py
print("Hello World from Python")
```

Detta kommer att skriva ut följande i konsolfönstret.

```cmd
Hello World from Python
```

Obs: Om du använder IDE, tillhandahåller de knappar på skärmen eller olika kortkommandon för att köra Python. Till exempel visas en spelknapp i rännstenen med editorn i PyCharm som låter dig köra Python-skriptet.

## PY-filformat ##

Python designades för läsbarhet och har likheter med engelska och matematik. Python använder nya rader för att indikera hela kommandot i motsats till semikolon eller parentes som används på andra språk. För scopes, loops och funktioner, förlitar Python sig på indrag och blanksteg i motsats till lockiga klammerparenteser som används på andra språk.

### Syntax ###

Följande är ett exempel på Python-syntax.

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

## Referenser ##

- [Python (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

