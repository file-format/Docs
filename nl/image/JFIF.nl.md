---
date: 2020-08-12
keywords: jfif, .jfif, jfif-bestandsindeling, hoe jfif-bestanden te openen, .jfif-extensie, jfif-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF-bestand - Wat is een .jfif-bestand?
linktitle: JFIF
description: "Meer informatie over de JFIF-bestandsindeling en API's die JFIF-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Wat is een JFIF-bestand?

JFIF (JPEG File Interchange Format (JFIF)) is een afbeeldingsbestand dat de .jfif-extensie gebruikt. JFIF bouwt over JIF (JPEG Interchange Format) door de complexiteit te verminderen en de beperkingen op te lossen.

## Korte geschiedenis van JFIF

De ontwikkeling van JFIF-documenten werd geleid door Eric Hamilton en eind 1991 werd overeenstemming bereikt over de eerste versie. Versie 1.02 werd op 7 september 1992 gepubliceerd. RFC 2046 specificeerde dat het JFIF-formaat wordt gebruikt om JPEG-afbeeldingen via internet te verzenden. JFIF werd in 2009 door ECMA gepubliceerd en werd in 2011 door ITU-T gestandaardiseerd als zijn aanbeveling T.871 en door ISO/IEC in 2013 als ISO/IEC 10918-5

## JFIF-bestandsindeling ##

Een JFIF-bestand bestaat uit een reeks markeringen zoals gedefinieerd in deel 1 van de JPEG-standaard. Elke markering bestaat uit twee bytes (FF gevolgd door een byte die het type markering aangeeft). Markers kunnen op zichzelf staan of het begin van een markersegment aangeven.

JFIF staat meerdere componenten zoals Y, Cb, Cr toe om verschillende resoluties te hebben, maar hun uitlijning is niet gedefinieerd. In tegenstelling tot JPEG kan JFIF informatie over resolutie en beeldverhouding leveren. JFIF definieert ook het te gebruiken kleurmodel.

### Bestandsstructuur ##

|Segment|Code|Beschrijving|
|---|---|---|
|SOI|FF D8|Begin van afbeelding|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|extra markeringssegmenten|
|SOS|FF DA|Begin van scan|
||gecomprimeerde afbeeldingsgegevens||
|EOI|FF D9|Einde van afbeelding|

De JFIF-standaard definieert de volgende segmenten:

### JFIF APP0-markeringssegment ###

Het is een verplicht segment dat afbeeldingsparameters bevat. Het kan ook een ingesloten niet-gecomprimeerde miniatuur bevatten.

|Veld|Grootte (bytes)|Beschrijving|
|---|---|---|
|APP0-markering|2|FF E0|
|Lengte|2|Lengte van segment exclusief APP0-markering|
|Identifier|5|JFIF (4A 46 49 46 00) in ASCII afgesloten met een null-byte|
|JFIF-versie|2|Versie van de JFIF|
|Dichtheidseenheden|1|Eenheid voor de volgende pixeldichtheidsvelden</br> 00 : Geen eenheden; breedte:hoogte pixelverhouding is gelijk aan Ydensity:Xdensity</br> 01: Pixels per inch</br> 02 : Pixels per centimeter|
|Xdensity|2|Horizontale pixeldichtheid groter dan nul|
|Ydensity|2|Verticale pixeldichtheid groter dan nul|
|Xthumbnail|1|Horizontaal aantal pixels van de ingesloten RGB-miniatuur. Kan nul zijn|
|Ythumbnail|1|Verticale aantal pixels van de ingesloten RGB-miniatuur. Kan nul zijn|
|Miniatuurgegevens|3 × n|Ongecomprimeerde 24-bits RGB-rasterminiatuurgegevens|

### JFIF-extensie APP0-markeringssegment ###

Dit is een optionele sectie die, indien gedefinieerd, onmiddellijk moet volgen op het JFIF APP0-markeringssegment. Deze sectie wordt ondersteund door JFIF versie 1.02 en hoger en maakt het insluiten van miniaturen in drie verschillende formaten mogelijk.

|Veld|Grootte (bytes)|Beschrijving|
|---|---|---|
|APP0-markering|2|FF E0|
|Length|2|Lengte van het segment exclusief APP0-markering|
|Identifier|5|JFXX (4A 46 58 58 00) in ASCII afgesloten met een null-byte|
|Miniatuurformaat|1|Geeft aan welk gegevensformaat wordt gebruikt voor de volgende ingebedde miniatuur:</br> 10 : JPEG-indeling</br> 11: 1 byte per pixel gepalettiseerd formaat</br> 13 : 3 byte per pixel RGB-formaat|
|Miniatuurgegevens|variabele||

## Conversie van JFIF naar andere afbeeldingsbestandsindelingen

JFIF kan worden geconverteerd naar populaire bestandsindelingen voor afbeeldingen, zoals [PNG](/nl/image/png/), [JPG](/nl/image/jpeg/) en [PDF](/nl/pdf/).

## Referenties ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

