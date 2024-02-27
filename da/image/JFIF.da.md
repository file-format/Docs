---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF-fil - Hvad er en .jfif-file?
linktitle: JFIF
description: Ltjene om JFIF filformat og API'er, der kan oprette og åbne JFIF fils.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Hvad er en JFIF fil?

JFIF (JPEG File Interchange Format (JFIF)) er en billedformatfil, der bruger filtypen .jfif. JFIF bygger over JIF (JPEG Interchange Format) ved at reducere kompleksiteten og løse dens begrænsninger.

## Kort historie om JFIF

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. Version 1.02 blev offentliggjort den 7. september 1992. RFC 2046 specificerede, at JFIF-formatet bruges til at overføre JPEG-billeder over internettet. JFIF blev udgivet af ECMA i 2009 og blev standardiseret af ITU-T i 2011 som dens anbefaling T.871 og af ISO/IEC i 2013 som ISO/IEC 10918-5

## JFIF filformat ##

En JFIF-fil består af en sekvens af markører som defineret i del 1 af JPEG-standarden. Hver markør består af to bytes (FF efterfulgt af en byte, der specificerer typen af markør). Markører kan enten være selvstændige eller angive starten på et markørsegment.

JFIF tillader flere komponenter som Y, Cb, Cr at have forskellige opløsninger, men deres justering er ikke defineret. I modsætning til JPEG kan JFIF give oplysninger om opløsning og billedformat. JFIF definerer også den farvemodel, der skal bruges.

### Filstruktur ##

|Segment|Kode|Beskrivelse|
|---|---|---|
|SOI|FF D8|Start af billede|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|yderligere markørsegmenter|
|SOS|FF DA|Start af scanning|
||komprimerede billeddata||
|EOI|FF D9|Slut på billede|

JFIF-standarden definerer følgende segmenter:

### JFIF APP0 markørsegment ###

Det er et obligatorisk segment, der indeholder billedparametre. Den kan også indeholde et indlejret ukomprimeret miniaturebillede.

|Felt|Størrelse (bytes)|Beskrivelse|
|---|---|---|
|APP0 markør|2|FF E0|
|Længde|2|Længde af segment eksklusiv APP0 markør|
|Identifier|5|JFIF (4A 46 49 46 00) i ASCII afsluttet af en null-byte|
|JFIF version|2|Version af JFIF|
|Densitetsenheder|1|Enhed for følgende pixeltæthedsfelter</br> 00 : Ingen enheder; bredde:højde pixelformatforhold er lig med Ydensity:Xdensity</br> 01 : Pixel pr. tomme</br> 02 : Pixel pr. centimeter|
|Xdensity|2|Horizontal pixeltæthed større end nul|
|Ydensity|2|Lodret pixeltæthed større end nul|
|Xthumbnail|1|Horizontalt pixelantal for det indlejrede RGB-miniaturebillede. Kan være nul|
|Ythumbnail|1|Lodret pixelantal for det indlejrede RGB-miniaturebillede. Kan være nul|
|Thumbnail data|3 × n|Ukomprimerede 24 bit RGB raster thumbnail data|

### JFIF-udvidelse APP0 markørsegment ###

Dette er en valgfri sektion, der, hvis den er defineret, umiddelbart skal følge JFIF APP0-markørsegmentet. Dette afsnit understøttes af JFIF version 1.02 og nyere og tillader indlejring af miniaturebilleder i tre forskellige formater.

|Felt|Størrelse (bytes)|Beskrivelse|
|---|---|---|
|APP0 markør|2|FF E0|
|Længde|2|Længde af segmentet eksklusive APP0-markør|
|Identifier|5|JFXX (4A 46 58 58 00) i ASCII afsluttet med en null-byte|
|Thumbnail format|1|Specificerer hvilket dataformat der bruges til følgende indlejrede miniature:</br> 10: JPEG-format</br> 11 : 1 byte pr. pixel palettiseret format</br> 13 : 3 byte pr. pixel RGB-format|
|Thumbnail data|variabel||

## Konvertering af JFIF til andre billedfilformater

JFIF kan konverteres til populære billedfilformater såsom [PNG](/image/png/), [JPG](/image/jpeg/) og [PDF](/pdf/).

## Referencer ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

