---
date: 2019-10-11
keywords: vob, .vob, vob-bestandsformaat, .vob-bestandsformaat, .vob-extensie, vob-extensie, vob-videoformaat, vob dvd-bestanden
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Leer over VOB-bestandsindelingen en API's die VOB-bestanden kunnen maken en openen."
title: VOB-bestandsindeling
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Wat is een VOB-bestand? ##

VOB-bestanden worden meestal opgeslagen in de VIDEO_TS-directory op een dvd met de extensie .vob. VOB-bestanden bevatten video- en audiogegevens, evenals andere gegevens zoals menu's en ondertitels. VOB is gebaseerd op het MPEG-2-programmastreamformaat, maar het heeft extra beperkingen en specificaties in privéstreams. VOB-bestanden zijn een strikte subset van MPEG-programmastreams, dus alle VOB-bestanden zijn MPEG-programmastreams, maar alle MPEG-programmastreams zijn niet VOB-compatibel.

## Structuur van dvd-video ##

Wanneer een dvd op een computer wordt geopend, is VIDEO_TS de map op het hoogste niveau met AUDIO_TS. AUDIO_TS is leeg en wordt niet gebruikt. In de VIDEO_TS-directory bevinden zich VOB-, BUP- en IFO-bestanden. VOB-bestanden bevatten de MPEG-inhoud. Deze zijn opgedeeld in brokken van 1 GB of minder, zodat deze compatibel zijn met alle besturingssystemen. De IFO-bestanden bevatten informatie over de menu's en de titelstructuur. De BUK-bestanden zijn back-upbestanden van de IFO-bestanden met dezelfde naam. Deze bestanden zijn bedoeld om fysiek in een aparte ruimte te worden bewaard, zodat in het geval dat het IFO-bestand beschadigd is door fysieke schade aan de dvd, het BUK-bestand dezelfde informatie kan bieden.

### Fysieke lay-out ###

- Alle bestanden op de schijf moeten aaneengesloten zijn.
- De gerelateerde bestanden moeten naast elkaar staan (VOB, IFO, BUP).
- De genummerde bestanden moeten in oplopende volgorde staan.

## Kopieerbeveiliging ##

Veel video-dvd's zijn gecodeerd en voorkomen het kopiëren van gegevens van de dvd. Authenticatie- en decoderingssleutels zijn nodig om de bestanden af te spelen die zich in het ontoegankelijke invoergebied van de dvd bevinden. Deze sleutels worden gebruikt door de CSS-decoderingssoftware die aanwezig is in de dvd-speler of de softwarespeler. Zonder de sleutels kunnen de videobestanden niet worden afgespeeld, omdat de sleutels worden gevraagd wanneer de bestanden worden geopend.

## Referenties ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

