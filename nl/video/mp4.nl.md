---
date: 2019-10-11
keywords: MP4, bestand, extensie, formaat, videoformaat, MPEG-4
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lees meer over de MP4-bestandsindeling en API's die MP4-bestanden kunnen maken en openen."
title: MP4-bestandsindeling
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Wat is een MP4-bestand? ##

MP4 (afkorting van MPEG-4 Part 14) is een bestandsindeling op basis van ISO/IEC 14496-12:2004 die is gebaseerd op QuickTime-bestandsindeling, maar die formeel ondersteuning biedt voor Initial Object Descriptors (IOD) en andere MPEG-functies. Het wordt meestal gebruikt om video en audio op te slaan, maar kan ook worden gebruikt om ondertitels en stilstaande beelden op te slaan. MP4-bestanden worden opgeslagen met de extensie .mp4. MP4 is een internationale audiovisuele coderingsstandaard. Net als de meeste moderne containerformaten, ondersteunt MP4 streaming via internet. Vanwege de hoge compressie die in MP4 wordt gebruikt, zijn de resulterende bestanden kleiner en behouden ze bijna alle oorspronkelijke kwaliteit.

## Korte geschiedenis ##

De MP4-specificatie is ontwikkeld door Moving Picture Experts Group (MPEG) en was gebaseerd op het QuickTime-formaat [MOV](/nl/video/mov/) dat in 2001 werd gepubliceerd. De eerste versie (ISO/IEC 14496-1:2001) van MP4 was een herziening van de MPEG-4 Deel 1: Systeemspecificatie gepubliceerd in 1999. Het MP4-bestandsformaat werd gegeneraliseerd naar ISO Base Media File Format ISO/IEC 14496-12:2004 dat de algemene structuur voor tijdgebaseerde mediabestanden definieerde. Als gevolg hiervan wordt het gebruikt als basis voor andere bestandsindelingen.

## Structuur van MP4-bestanden ##

MP4 is een uitbreidbaar containerbestand, wat betekent dat het geen strikte structuur definieert en een aangepaste structuur en hiërarchie toestaat voor elk mediatype. De gegevens in het MP4-bestand zijn verdeeld in twee secties, de eerste met de mediagerelateerde gegevens en de tweede met metagegevens. De mediagegevens bevatten audio of video en metagegevens geven vlaggen aan voor willekeurige toegang, tijdstempels, enz.
De structuren in MP4 worden meestal atomen of dozen genoemd. De minimale grootte van een atoom is 8 bytes (de eerste 4 bytes specificeren de grootte en de volgende 4 bytes specificeren het type). Hier is een lijst van de atomen op rootniveau in MP-bestanden:

- **ftyp**: bevat het bestandstype, de beschrijving en de veelgebruikte datastructuren.
- **pdin**: bevat informatie over het progressief laden/downloaden van video's.
- **moov**: container voor alle metadata van films.
- **moof**: container met videofragmenten.
- **mfra**: De container met willekeurige toegang tot het videofragment
- **mdat**: gegevenscontainer voor media.
- **stts**: voorbeeld-naar-tijdtabel.
- **stsc**: tabel van monster naar stuk.
- **stsz**: steekproefomvang (framing)
- **meta**: de container met de metadata-informatie.

Hier is een lijst met atomen van het tweede niveau die in MP4 worden gebruikt:

- **mvhd**: bevat de videokopinformatie met volledige details van de video.
- **trak**: Container met de individuele track.
- **udta**: de container met de gebruikers- en trackinformatie.
- **iods**: MP4-bestandsbeschrijving

## Referenties ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

