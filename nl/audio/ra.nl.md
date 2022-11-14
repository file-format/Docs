---
date: 2019-12-13
keywords: ra, ra-bestandsformaat, .ra-extensie, echt audiobestandsformaat, ra-audioformaat, RealAudio-bestandsformaat
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over RA-bestandsindelingen en API's die RA-bestanden kunnen maken en openen."
title: RA-bestandsindeling
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## Wat is een RA-bestand?

RealAudio (RA) is een eigen audioformaat ontwikkeld door Real Networks, Inc. en uitgebracht in april 1995. Het gebruikt de .ra-extensie voor zijn bestanden. Het maakt gebruik van zowel low-bitrate als high-fidelity audiocodecs. RA werd door veel internetradiostations gebruikt voor audiostreaming via internet. De BBC-website gebruikte RA tot 2009 intensief, maar stopte in maart 2011.

## Bestandsextensie door RealNetworks ##

RealNetworks gebruikte het RA-bestandsformaat voor audio. RealNetworks begon in 1997 met het aanbieden van videoformaat ([RealVideo](/nl/video/rv/)) met de .rv-extensie. [RealMedia (RM)](/nl/video/rm/) werd gebruikt voor de combinatie van audio- en videoformaten. Met de nieuwste release van RealProduce (Real's encoder) wordt het RV-formaat gebruikt voor videobestanden en wordt het [RealMedia Variable Bitrate (RMVB)](/nl/video/rmvb/)-formaat gebruikt voor VBR-videobestanden (Variable bitrate).

## Audio streamen ##

RA is ontwikkeld als streaming media-formaat en kan worden gestreamd met HTTP. Het audiobestand begint te spelen zodra het eerste deel van het bestand is ontvangen en blijft spelen terwijl de rest van het bestand wordt gedownload.

De eerste versie van de RealAudio gebruikte het gepatenteerde PNA- of PNM-protocol om audio te streamen. Later schakelden ze over op IETF-gestandaardiseerde RTSP (Real Time Streaming Protocol) om verbindingen te beheren. Voor het verzenden van gegevens gebruikten ze het RDT-protocol (Real Data Transfer). Het protocol werd aanvankelijk geheim gehouden, maar later werd een deel ervan openbaar gemaakt via het Helix-project.

Om RealAudio-bestanden te streamen, linken de meeste pagina's naar het RAM-bestand (Real Audio Metadata) of SMIL (Synchronized Multimedia Integration Language). Dit bestand wordt gebruikt om de mediaspeler van de gebruiker te laden en de audio te streamen vanaf de URL in het bestand.

## RealAudio Audio-codecs ##

Hier is een lijst met audiocodecs die elk worden geïdentificeerd door een code van vier tekens, samen met de versie van RealAudio die deze heeft geïntroduceerd.

|Codec|RealAudio-versie|
|---|---|
|lpcJ en 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|kok|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## Referenties ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

