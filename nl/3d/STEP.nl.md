---
date: 2019-10-11
keywords: stap, .stap, stap bestandsformaat, hoe stap bestanden te openen, .stap extensie, stap extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP-bestandsindeling
linktitle: STEP
description: "Lees meer over de STEP-bestandsindeling en API's die STEP-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Wat is een STEP-bestand?

STEP-bestand is een veelgebruikt formaat voor gegevensuitwisseling voor computerondersteund ontwerp (CAD). Het werd in 1994 gestandaardiseerd door de ISO-commissie onder de naam "ISO 10303-21". ISO 10303-21 definieert het coderingsmechanisme voor het weergeven van gegevens in EXPRESS-taal voor gegevensmodellering. Een STEP-bestand wordt ook wel p21-File en STEP Physical File genoemd. De bestandsextensies die gebruikt worden voor STEP-file zijn .stp en .step.

## Basisgeschiedenis

In 1994 werd de originele Part 21-specificatie uitgegeven. Het bevat een aantal fouten die zijn gecorrigeerd door de technische rectificatie die in 1996 is uitgegeven. De tweede editie werd in 2002 gepubliceerd en bevatte de rectificatie en uitbreidingen voor verschillende gegevenssecties. De derde editie werd in 2016 gepubliceerd met anker- en referentiesecties waarmee entiteiten en waarden in externe bestanden konden worden opgeslagen. UTF-8-ondersteuning is toegevoegd van strings. Er werden digitale handtekeningen toegevoegd om de inhoud van het bestand te verifiëren en de referenties te valideren. De ondersteuning voor het comprimeren en opslaan van de uitwisselingsstructuur met behulp van ZIP werd ook toegevoegd.

## STEP-bestandsindeling

Het platte tekstformaat voor een STEP-bestand bestaat uit een reeks records. De tekenset is gedefinieerd als codepunten van ISO 10646. "ISO-10303-21;" zijn de eerste tekens in de eerste record. Opmerkingen zijn omgeven door tekens "/*" en "*/". Het laatste record bevat "END-ISO-10303-21;" als het STEP-bestand overeenkomt met de 2002-versie. Als het overeenkomt met de 2016-versie, kunnen er een of meer digitale handtekeningen staan na de "END-ISO-10303-21;" terminator. Regeleinden worden aangegeven met "\N\" en pagina-einden worden aangegeven met "\F\".

Het STEP-bestand is onderverdeeld in secties en hun namen zijn gereserveerde termen. Alle secties eindigen met het record "ENDSEC" en moeten in de onderstaande volgorde staan.

- **HEADER**: dit is een verplichte en niet-herhaalbare sectie. Het bestaat uit de volgende entiteiten:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: het is een optionele niet-herhalende sectie die werd geïntroduceerd in de 2016-versie. Het definieert de externe namen voor instanties, zodat ernaar kan worden verwezen.
- **REFERENTIE**: het is een optionele niet-herhalende sectie die ook werd geïntroduceerd in de 2016-versie. Elk item in deze sectie koppelt een item/waarde-instantienaam aan een instantie/waarde in een extern bestand.
- **GEGEVENS**: het is een optionele herhaalbare sectie die de kerninhoud van de modelinstantie bevat.
- ** HANDTEKENING **: het is een optioneel herhaalbaar gedeelte dat werd geïntroduceerd in de 2016-versie. Het bevat de digitale handtekening om de inhoud van het bestand te verifiëren of om referenties te valideren.

## Referenties

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

