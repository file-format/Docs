---
date: 2019-10-11
keywords: py, python, .py, py bestandsformaat, hoe py-bestand te openen, hoe py-bestanden uit te voeren, hoe python-bestanden uit te voeren, hoe python uit te voeren
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY-bestandsindeling
linktitle: PY
description: "Lees meer over de PY-bestandsindeling en API's die PY-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Wat is een PY-bestand? ##

De bestanden met de extensie .py bevatten de Python-broncode. De Python-taal is tegenwoordig een zeer bekende taal geworden. Het kan worden gebruikt voor systeemscripting, web- en softwareontwikkeling en wiskunde. Python ondersteunt platformonafhankelijke compatibiliteit; betekent dat de ontwikkelde applicaties in Python op verschillende platforms kunnen werken, zoals Windows, MAC, Linux, Raspberry Pi, enz. Python biedt een eenvoudige en gemakkelijk te lezen syntaxis die vergelijkbaar is met de Engelse taal. Ontwikkelaars kunnen een redelijke softwaretoepassing schrijven door een paar regels Python-code te schrijven. Omdat de Python op een interpretersysteem draait, kan de code worden uitgevoerd zodra deze is geschreven, wat hem zeer goed maakt voor prototyping.

## Korte geschiedenis ##

Python is eind jaren tachtig bedacht door Guido van Rossum als opvolger van de programmeertaal ABC. De implementatie begon in december 1989 met Van Rossum als enige hoofdontwikkelaar. Hij werkte aan Python tot 12 juli 2018. In januari 2019 kozen de actieve Python-kernontwikkelaars een vijfkoppige "Steering Council" bestaande uit Nick Coghlan, Brett Cannon, Carol Willing, Barry Warschau en Van Rossum om het project te leiden.

### Versies ###

- Python 2.0 werd uitgebracht op 16 oktober 2000.
- Python 3.0 werd uitgebracht op 3 december 2008.

## Hoe py-bestand ## uit te voeren

Om de geïnstalleerde versie van Python te controleren, kunt u de volgende opdracht gebruiken:

```cmd
python --version
```

Dit zal de versie op de console uitvoeren zoals

```cmd
Python 3.7.4
```

Als Python niet op uw computer is geïnstalleerd, kunt u naar [python.org](https://www.python.org/) gaan en Python downloaden en installeren voor uw relevante besturingssysteem.

Om een Python-script uit te voeren, kunt u het volgende commando gebruiken:

```cmd
python helloworld.py
```

*helloworld.py* is een scriptbestand dat de volgende code bevat:

```py
print("Hello World from Python")
```

Hierdoor wordt het volgende afgedrukt in het consolevenster.

```cmd
Hello World from Python
```

Opmerking: als u IDE's gebruikt, bieden ze knoppen op het scherm of verschillende sneltoetsen om Python uit te voeren. Er wordt bijvoorbeeld een afspeelknop getoond in de goot met de editor in PyCharm waarmee je het Python-script kunt uitvoeren.

## PY-bestandsindeling ##

Python is ontworpen voor leesbaarheid en heeft overeenkomsten met Engels en wiskunde. Python gebruikt nieuwe regels om het volledige commando aan te geven, in tegenstelling tot puntkomma's of haakjes die in andere talen worden gebruikt. Voor scopes, loops en functies vertrouwt Python op inspringing en witruimten in tegenstelling tot accolades die in andere talen worden gebruikt.

### Syntaxis ###

Het volgende is een voorbeeld van de Python-syntaxis.

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

## Referenties ##

- [Python (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

