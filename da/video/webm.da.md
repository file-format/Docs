---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltjene om WEBM filformat og API'er, der kan oprette og åbne WEBM fils.
title: WEBM - WebM-videofilformularat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Hvad er en WEBM fil?

En fil med filtypenavnet .webm er en videofil baseret på det åbne, royaltyfrie WebM-filformat. Den er designet til deling af video på nettet og definerer filbeholderstrukturen inklusive video- og lydformater. WebM er 100 % gratis og implementerer høj kvalitet baseret på åbne teknologier såsom HTML, HTTP og TCP/IP, som er åbne for alle til implementering. WebM er specielt designet til at vise video på nettet, hvilket gør det optimeret til streaming med et lavt beregningsmæssigt fodaftryk. Dette gør den velegnet til afspilning af videoer på enhver enhed, især netbooks, håndholdte og tablets med lavt strømforbrug.

## WEBM filformat

WebM-filstrukturen er baseret på et undersæt af Matroska [MKV](/video/mkv/) containerfilformat. De tilgængelige videostreams i en WebM-fil komprimeres ved hjælp af VP8- eller VP9-komprimeringsteknologier, der er yderst effektive i komprimering. På samme måde komprimeres lydstrømmene i en WebM-fil ved hjælp af Vorbis- eller Opus-codecs, der blev udviklet af [Xiph Foundation](https://www.xiph.org/). Alle disse videoer og lyd-codecs er royaltyfrie og kan bruges uden omkostninger.

Følgende er de opsummerede specifikationer for WebM-filformatet.

|Felt|Beskrivelse|
---|---|
|MIME-type |video/webm|
|Lyd-kun MIME-type |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Video Codec Navn| VP8 eller VP9|
|Lyd Codec Navn| Vorbis eller Opus|

### WebM Elements

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Navn |Beskrivelse|
---|---|
|EBML|Indstil EBML-egenskaberne for de data, der skal følges. Hvert EBML-dokument skal starte med dette.|
|EBMLVersion |Versionen af EBML-parseren, der blev brugt til at oprette filen.|
|EBMLReadVersion|Den mindste EBML-version, som en parser skal understøtte for at læse denne fil.|
|EBMLMaxIDLength |Den maksimale længde af de ID'er, du finder i denne fil (4 eller mindre i Matroska).|
|EBMLMaxSizeLength|Den maksimale længde af størrelserne, du finder i denne fil (8 eller mindre i Matroska). Dette tilsidesætter ikke elementstørrelsen angivet i begyndelsen af et element. Elementer, der har en angivet størrelse, der er større end det, der er tilladt af EBMLMaxSizeLength, betragtes som ugyldige.|
|DocType|En streng, der beskriver den type dokument, der følger denne EBML-header (webm i vores tilfælde).|
|DocTypeVersion|Versionen af DocType-fortolkeren, der blev brugt til at oprette filen.|
|DocTypeReadVersion|Den mindste DocType-version, som en tolk skal understøtte for at læse denne fil.|

#### Globale elementer

I øjeblikket understøttes kun Void-elementet, der bruges til at annullere beskadigede data, for at undgå uventet adfærd ved brug af beskadigede data. Indholdet kasseres. Bruges også til at reservere plads i et underelement til senere brug.

#### Segment
Dette element indeholder alle andre elementer på øverste niveau (niveau 1). Typisk er en Matroska-fil sammensat af 1 segment.

#### Meta Søg information

Følgende søgeoplysninger understøttes.

|Elementnavn |Beskrivelse|
---|---|
|SeekHead |Indeholder positionen for et andet niveau 1-element.|
|Seek |Indeholder en enkelt søgepost til et EBML-element.|
|SeekID |Det binære ID, der svarer til elementnavnet.|
|SeekPosition |Placeringen af elementet i segmentet i oktetter (0 = første niveau 1 element).|

## Referencer

* [WebM](https://www.webmproject.org/)

* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)


