---
date: 2019-10-11
keywords: WEBM, Wat is een WEBM-bestand, WEBM-bestandsindeling
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Meer informatie over WEBM-bestandsindelingen en API's waarmee WEBM-bestanden kunnen worden gemaakt en geopend."
title: WEBM - WebM-videobestandsindeling
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Wat is een WEBM-bestand?

Een bestand met de extensie .webm is een videobestand dat is gebaseerd op het open, royaltyvrije WebM-bestandsformaat. Het is ontworpen voor het delen van video op het web en definieert de bestandscontainerstructuur, inclusief video- en audioformaten. WebM is 100% gratis en implementeert hoge kwaliteit op basis van open technologieën zoals HTML, HTTP en TCP/IP die voor iedereen toegankelijk zijn voor implementatie. WebM is speciaal ontworpen voor het aanbieden van video op het web, waardoor het geoptimaliseerd is voor streaming met een lage computationele voetafdruk. Dit maakt het geschikt voor het afspelen van video's op elk apparaat, met name netbooks, handhelds en tablets met een laag stroomverbruik.

## WEBM-bestandsindeling

De WebM-bestandsstructuur is gebaseerd op een subset van het Matroska [MKV](/nl/video/mkv/) containerbestandsformaat. De videostreams die beschikbaar zijn in een WebM-bestand worden gecomprimeerd met behulp van de VP8- of VP9-compressietechnologieën die zeer efficiënt zijn in compressie. Op dezelfde manier worden de audiostreams in een WebM-bestand gecomprimeerd met behulp van de Vorbis- of Opus-codecs die zijn ontwikkeld door de [Xiph Foundation](https://www.xiph.org/). Al deze video- en audiocodecs zijn royaltyvrij en kunnen gratis worden gebruikt.

Hieronder volgen de samengevatte specificaties voor het WebM-bestandsformaat.

|Veld|Beschrijving|
---|---|
|MIME-type |video/webm|
|Alleen audio MIME-type |audio/webm|
|Uniform type-ID| org.webmproject.webm|
|Naam videocodec| VP8 of VP9|
|Audiocodec-naam| Vorbis of Opus|

### WebM-elementen

WebM, dat een subset is van de Matroska-specificaties, biedt ondersteuning voor een deel van de Matroska-functionaliteit. Hieronder volgt een beschrijving van de ondersteunde elementen.

#### EBML

|Naam |Beschrijving|
---|---|
|EBML|Stel de EBML-kenmerken van de te volgen gegevens in. Elk EBML-document moet hiermee beginnen.|
|EBMLVersion |De versie van de EBML-parser die is gebruikt om het bestand te maken.|
|EBMLReadVersion|De minimale EBML-versie die een parser moet ondersteunen om dit bestand te lezen.|
|EBMLMaxIDLength |De maximale lengte van de ID's die u in dit bestand vindt (4 of minder in Matroska).|
|EBMLMaxSizeLength|De maximale lengte van de maten die je in dit bestand vindt (8 of minder in Matroska). Dit heeft geen voorrang op de elementgrootte die aan het begin van een element is aangegeven. Elementen met een aangegeven afmeting die groter is dan toegestaan door EBMLMaxSizeLength worden als ongeldig beschouwd.|
|DocType|Een tekenreeks die het type document beschrijft dat volgt op deze EBML-header ("webm" in ons geval).|
|DocTypeVersion|De versie van de DocType-interpreter die is gebruikt om het bestand te maken.|
|DocTypeReadVersion|De minimale DocType-versie die een tolk moet ondersteunen om dit bestand te lezen.|

#### Globale elementen

Op dit moment wordt alleen het `Void`-element ondersteund dat wordt gebruikt om beschadigde gegevens ongeldig te maken, om onverwacht gedrag bij het gebruik van beschadigde gegevens te voorkomen. De inhoud wordt weggegooid. Wordt ook gebruikt om ruimte in een subelement te reserveren voor later gebruik.

#### Segment
Dit element bevat alle andere elementen op het hoogste niveau (niveau 1). Typisch bestaat een Matroska-bestand uit 1 segment.

#### Meta zoeken naar informatie

De volgende informatie zoeken wordt ondersteund.

|Elementnaam |Beschrijving|
---|---|
|SeekHead |Bevat de positie van een ander niveau 1 element.|
|Seek |Bevat een enkele zoekingang naar een EBML-element.|
|SeekID |De binaire ID die overeenkomt met de elementnaam.|
|SeekPosition |De positie van het element in het segment in octetten (0 = eerste niveau 1 element).|

## Referenties

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)

