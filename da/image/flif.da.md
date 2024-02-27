---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF fil formularat
linktitle: FLIF
description: Ltjen om FLIF filformat og API'er, der kan oprette og åbne FLIF fils.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Hvad er en FLIF fil? ##

FLIF (Free Lossless Image Format) er et tabsfrit billedformat, der bruger filtypenavnet .flif til sine filer. FLIF hævder at overgå [PNG](/image/png/), tabsfri [WebP](/image/webp/), tabsfri BPG og tabsfri JPEG 2000 med hensyn til kompressionsforhold. FLIF bruger progressiv interlacing, på grund af hvilken enhver delvis download af billedet kan bruges som en tabsgivende kodning for hele billedet.

## Kort historie ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. I september 2016 blev den første stabile version af FLIF udgivet.

## FLIF Design ##

FLIF bruger en variant af CABAC (Context-adaptive binary aritmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) til komprimering. MANIAC er en entropikodningsalgoritme udviklet af Jon Sneyers og Pieter Wuille. I MANIAC er sammenhængene noder af beslutningstræer, der læres dynamisk ved indkodningstid. Dette gør kontekstmodellen mere billedspecifik og resulterer i en bedre komprimering. FLIF har følgende funktioner:

- Understøtter tabsfri kompression
- Understøtter tabsgivende komprimering med encoder-forbehandling
- Understøtter gråtoner, RGB og RGBA
- Understøtter farvedybde på 1 til 16 bit pr. kanal
- Understøtter sammenflettede og ikke-sammenflettede filer
- Understøtter progressiv afkodning af delvist downloadede filer
- Understøtter animationer
- Understøtter indlejrede ICC-farveprofiler, Exif- og XMP-metadata
- Har begrænset understøttelse af komprimering af Camera Raw-filer (RGGB)

## FLIF filformat ##

En FLIF-fil har følgende fire dele:

## Hovedoverskrift ##

Hovedhovedet indeholder de vigtigste metadata inklusive bredde, højde, farvedybde, antal rammer.

|Type|Værdi|Beskrivelse|
|---|---|---|
|4 bytes|FLIF|Magic|
|4 bit|3 = ni stadig; 4 = i stadig; 5 = ni dyr; 6 = i anim|Interlacing, animation|
|4 bit|1 = Gråtoner; 3 = RGB; 4 = RGBA|Antal kanaler (nb_kanaler)|
|1 byte|'0','1','2' ('0'=custom)|Bytes pr. kanal (Bpc)|
|varint|width-1|Bredde|
|varint|højde-1|Højde|
|varint|nb_frames-2 (kun hvis animation)|Antal rammer (nb_frames)|

## Metadata bidder ##

Denne del indeholder ikke-pixel som Exif/XMP-metadata, ICC-farveprofil osv., der er kodet ved hjælp af DEFLATE-komprimering. Disse chunks er defineret på samme måde som PNG chunks med forskellen, at chuckstørrelsen er kodet med et variabelt antal bytes. Chunks' navne kan være på 4 bogstaver (4 bytes) eller en værdi under 32, hvilket indikerer en ikke-valgfri chunk.

Følgende er et eksempel på valgfri spændepatroner:

|Kunknavn|Beskrivelse|Indhold (efter DEFLATE-dekompression)|
|---|---|---|
|iCCP|ICC farveprofil|rå ICC farveprofildata|
|eXif|Exif-metadata|Exif\0\0-header efterfulgt af en TIFF-header og EXIF-data|
|eXmp|XMP-metadata|XMP indeholdt i en skrivebeskyttet x-pakke uden udfyldning|

### Navnekonvention ###

- **Første bogstav**: Store bogstaver bruges til kritiske og små bogstaver bruges til ikke-kritiske bidder.
- **Andet bogstav**: Store bogstaver bruges til offentlige og små bogstaver bruges til private bidder
- **Tredje bogstav**: Store bogstaver bruges til patroner, der er nødvendige for at vise billedet korrekt, og små bogstaver er ikke vigtige for at vise billedet.
- **Fjerde bogstav**: Store bogstaver bruges til patroner, der sikkert kan kopieres blindt. Små patroner afhænger af billeddataene.

## Anden overskrift ##

Dette indeholder oplysninger om den faktiske kodning af pixels.

|Type|Beskrivelse|Betingelse|Standardværdi|
|---|---|---|---|
|1 byte|NUL byte (0x00), delnavn på en FLIF16 bitstream||
|uni_int(1,16)|Bits pr. pixel af kanalerne|Bpc == '0': repeat(nb_channels)|8 hvis Bpc == '1', 16 hvis Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_kanaler > 3|0|
|uni_int(0,100)|Antal sløjfer|nb_frames > 1||
|uni_int(0,60_000)|Frame forsinkelse i ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flag: has_custom_cutoff_and_alpha|||
|uni_int(1.128)|cutoff|har_tilpasset_cutoff_and_alpha|2|
|uni_int(2.128)|alfa divisor|har_tilpasset_afskæring_og_alfa|19|
|uni_int(0,1)|Flag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|har_tilpasset_bitchance||
|variabel|Transformationer (se nedenfor)|||
|uni_int(1) = 0|Indikatorbit: udført med transformationer|||
|uni_int(0,2)|Usynlig pixel forudsigelse|alpha_zero && interlaced && alpha range inkluderer nul||

**Kanaler**

|Kanalnummer|Beskrivelse|
|---|----|
|0|Rød eller Grå|
|1|Grøn|
|2|Blå|
|3|Alfa|

**Transformationer**

|Type|Beskrivelse|
|---|---|
|uni_int(1) = 1|Indikatorbit: ikke udført endnu|
|uni_int(0,13)|Transformationsidentifikator|
|variabel|Transformationsdata (afhænger af transformation)|

Transformation bruges til at ændre pixeldata for bedre komprimering og til at holde styr på faktisk forekommende pixelværdier.

## Pixeldata ##

Denne del indeholder de faktiske pixeldata, der er kodet ved hjælp af MANIAC entropikodning. Pixels kan være kodet ved hjælp af interlaced eller ikke-interlaced kodning.

### Interlaced metode ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Med andre ord er hvert lige nummererede zoomniveau 2k en downsamplet version af billedet i skala 1:2^k. Zoomniveauer er kodet fra det højeste til det laveste.

### Ikke-sammenflettet metode ###

I denne metode begynder kodningen af MANIAC-træerne umiddelbart efterfulgt af kodningen af pixels.

## Referencer ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

