---
date: 2019-10-11
keywords: srt, .srt, srt bestandsformaat, .srt bestandsformaat, .srt extensie, srt extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over SRT-bestandsindelingen en API's die SRT-bestanden kunnen maken en openen."
title: SRT-bestandsindeling
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Wat is een SRT-bestand? ##

SRT (SubRip-bestandsindeling) is een eenvoudig ondertitelbestand dat is opgeslagen in de SubRip-bestandsindeling met de extensie .srt. Het bevat een opeenvolgend aantal ondertitels, start- en eindtijdstempels en ondertiteltekst. SRT-bestanden maken het mogelijk om ondertitels toe te voegen aan video-inhoud nadat deze is geproduceerd.

## SRT-bestand Structuur ##

Elke ondertitel heeft vier delen in het SRT-bestand.

1. Een numerieke teller die het nummer of de positie van de ondertitel aangeeft.
1. Begin- en eindtijd van de ondertitel gescheiden door --> tekens
1. Ondertiteltekst in één of meer regels.
1. Een lege regel die het einde van de ondertitel aangeeft.

### Voorbeeld van SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Om de tijd te specificeren wordt *hours:minutes:seconds,milliseconds (00:00:00,000)* formaat gebruikt.

## Opmaak van SRT-bestanden ##

De opmaak van SRT-bestanden is afgeleid van HTML-tags. De opmaaktags voor het SRT-bestand staan hieronder vermeld.

| Effect | Tags |
| --- | --- |
|Vet|**\ <b>...\</b> ** of {b}...{/b}|
|Cursief|**\ <i>...\</i> ** of **{i}...{/i}**|
|Onderstrepen|**\ <u>...\</u> ** of **{u}...{/u}**|
|Lettertypekleur|**\ <font color="white">...\</font> **|
|Line Position|**{\a3}** (geeft aan dat de tekst op regel 3 moet verschijnen)

## SubRip-software ##

SubRip is een gratis softwareprogramma dat op Windows draait. Het haalt ondertitels en hun timing uit verschillende videoformaten en slaat de ondertitels op in SRT-formaat. SubRip gebruikt optische tekenherkenning om ondertitels uit live video, andere videobestanden en dvd's te extraheren.

## Referenties ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
