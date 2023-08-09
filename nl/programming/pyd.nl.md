---
date: 2022-05-09
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD-bestandsindeling - Python dynamische module
linktitle: PYD
description: "Lees meer over de PYD-bestandsindeling en API's die PYD-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Wat is een PYD-bestand?

Een PYD-bestand is een dynamische linkbibliotheek die is geschreven in Python en die tijdens runtime door andere Python-code kan worden uitgevoerd. Het bevat een of meer Python-modules die hergebruik van code mogelijk maken en module-architectuur bieden voor het schrijven van applicaties. PYD-bestanden kunnen worden gemaakt en opgeslagen met de extensie .pyd, bijvoorbeeld helloworld.pyd. Applicatieontwikkelaars kunnen importstatement gebruiken om de PYD-modules in hun applicaties op te nemen. PYD-bestanden kunnen worden geopend met Python Software Foundation Python dat beschikbaar is voor Windows, Mac en Linux OS.

## PYD-bestandsindeling - Meer informatie

PYD-bestanden zijn geschreven in de programmeertaal Python en worden gegenereerd door de Python-code te compileren.

## Verschil tussen PY- en PYD-bestandsindelingen

Een [PY](/nl/programming/py/)-bestand bevat broncode die wordt uitgevoerd zoals deze is en niet kan worden opgenomen als herbruikbare code in andere Python-toepassingen. Een PYD-bestand is echter een dynamisch gekoppelde bibliotheek voor gebruik op het Windows-besturingssysteem.

## Hoe maak je een PYD-bestand aan?

Een PYD-bestand kan worden gemaakt door een module te maken met een naam, bijvoorbeeld exmaple.pyd. Deze module bevat alle functionaliteit in de vorm van een of meer functies, bijvoorbeeld PyMod_example(). Wanneer het programma deze bibliotheek bevat en deze aanroept, kan dit worden gedaan door de module te importeren en zal de functie PyMod_example() worden uitgevoerd.

## Referenties ##

* [Python-extensies maken in C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

