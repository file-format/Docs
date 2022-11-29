---
date: 2020-08-12
keywords: flif, .flif, flif filformat, hur man öppnar flif filer, .flif extension, flif extension
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF filformat
linktitle: FLIF
description: "Lär dig om FLIF-filformat och API:er som kan skapa och öppna FLIF-filer." 
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Vad är FLIF fil? ##

FLIF (Free Lossless Image Format) är ett förlustfritt bildformat som använder filtillägget .flif för sina filer. FLIF hävdar att de överträffar [PNG](/sv/image/png/), förlustfri [WebP](/sv/image/webp/), förlustfri BPG och förlustfri JPEG 2000 när det gäller kompressionsförhållande. FLIF använder progressiv sammanflätning, vilket gör att varje partiell nedladdning av bilden kan användas som en förlustkodning för hela bilden.

## Kortfattad bakgrund ##

FLIF tillkännagavs i september 2015, och alfaversionen släpptes i oktober 2015. I september 2016 släpptes den första stabila versionen av FLIF.

## FLIF Design ##

FLIF använder en variant av CABAC (Context-adaptive binary aritmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) för komprimering. MANIAC är en entropikodningsalgoritm utvecklad av Jon Sneyers och Pieter Wuille. I MANIAC är sammanhangen noder av beslutsträd som lärs in vid kodningstid dynamiskt. Detta gör kontextmodellen mer bildspecifik och ger en bättre komprimering. FLIF har följande funktioner:

- Stöder förlustfri komprimering
- Stöder förlustkomprimering med kodarförbearbetning
- Stöder gråskala, RGB och RGBA
- Stöder färgdjup på 1 till 16 bitar per kanal
- Stöder sammanflätade och icke-sammanflätade filer
- Stöder progressiv avkodning av delvis nedladdade filer
- Stöder animationer
- Stöder inbäddade ICC-färgprofiler, Exif- och XMP-metadata
- Har begränsat stöd för att komprimera Camera Raw-filer (RGGB)

## FLIF-filformat ##

En FLIF-fil har följande fyra delar:

## Huvudhuvud ##

Huvudhuvudet innehåller huvudmetadata inklusive bredd, höjd, färgdjup, antal ramar.

|Typ|Värde|Beskrivning|
|---|---|---|
|4 byte|"FLIF"|Magic|
|4 bitar|3 = ni still; 4 = jag fortfarande; 5 = ni djur; 6 = i anim|Interlacing, animation|
|4 bitar|1 = Gråskala; 3 = RGB; 4 = RGBA|Antal kanaler (nb_channels)|
|1 byte|'0','1','2' ('0'=custom)|Byte per kanal (Bpc)|
|varint|width-1|Bredd|
|varint|höjd-1|Höjd|
|varint|nb_frames-2 (endast om animering)|Antal bildrutor (nb_frames)|

## Metadatabitar ##

Den här delen innehåller icke-pixlar som Exif/XMP-metadata, ICC-färgprofil, etc. som är kodad med DEFLATE-komprimering. Dessa bitar definieras på liknande sätt som PNG-bitar med skillnaden att chuckstorleken är kodad med ett variabelt antal byte. Klumparnas namn kan vara 4 bokstäver (4 byte) eller ett värde under 32, vilket indikerar en icke-valfri chunk.

Följande är ett exempel på valfria chuckar:

|Chunknamn|Beskrivning|Innehåll (efter DEFLATE-dekompression)|
|---|---|---|
|iCCP|ICC-färgprofil|rå ICC-färgprofildata|
|eXif|Exif-metadata|"Exif\0\0"-rubrik följt av en TIFF-rubrik och EXIF-data|
|eXmp|XMP-metadata|XMP som finns i ett skrivskyddat xpaket utan utfyllnad|

### Namnkonvention ###

- **Första bokstav**: Versaler används för kritiska och gemener används för icke-kritiska bitar.
- **Andra bokstav**: Versaler används för offentliga och gemener används för privata bitar
- **Tredje bokstaven**: Versaler används för chuckar som behövs för att visa bilden korrekt och gemener är inte viktiga för att visa bilden.
- **Fjärde bokstaven**: Versaler används för chuckar som säkert kan kopieras blint. Små chuckar beror på bilddata.

## Andra rubrik ##

Detta innehåller information om den faktiska kodningen av pixlarna.

|Typ|Beskrivning|Skicka|Standardvärde|
|---|---|---|---|
|1 byte|NUL-byte (0x00), bitnamn på en FLIF16-bitström||
|uni_int(1,16)|Bitar per pixel av kanalerna|Bpc == '0': repeat(nb_channels)|8 om Bpc == '1', 16 om Bpc == '2'|
|uni_int(0,1)|Flagga: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Antal loopar|nb_frames > 1||
|uni_int(0,60_000)|Framfördröjning i ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flagga: has_custom_cutoff_and_alpha|||
|uni_int(1 128)|cutoff|har_anpassad_cutoff_and_alpha|2|
|uni_int(2 128)|alfadelare|har_anpassad_cutoff_and_alpha|19|
|uni_int(0,1)|Flagga: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|har_anpassad_bitchance||
|variabel|Transformationer (se nedan)|||
|uni_int(1) = 0|Indikatorbit: gjort med transformationer|||
|uni_int(0,2)|Osynlig pixelprediktor|alpha_noll && interlaced && alfaintervall inkluderar noll||

**Kanaler**

|Kanalnummer|Beskrivning|
|---|----|
|0|Röd eller Grå|
|1|Grön|
|2|Blå|
|3|Alfa|

**Förvandlingar**

|Typ|Beskrivning|
|---|---|
|uni_int(1) = 1|Indikatorbit: inte gjort ännu|
|uni_int(0,13)|Transformationsidentifierare|
|variabel|Transformationsdata (beror på transformation)|

Transformation används för att modifiera pixeldata för bättre komprimering och för att hålla reda på faktiskt förekommande pixelvärden.

## Pixeldata ##

Den här delen innehåller de faktiska pixeldata som kodats med hjälp av MANIAC-entropikodning. Pixlarna kan kodas med användning av interlaced eller icke-interlaced-kodning.

### Interlaced metod ###

I den här metoden definieras zoomnivåer. Zoomnivå 0 används för hela bilden, zoomnivå 1 används för alla jämna rader, zoomnivå 2 används för alla jämna kolumner på zoomnivå 1. Med andra ord är varje jämnt numrerad zoomnivå 2k en nedsamplad version av bild, i skala 1:2^k. Zoomnivåer kodas från den högsta till den lägsta.

### Non-interlaced metod ###

I denna metod börjar kodningen av MANIAC-träden omedelbart följt av kodningen av pixlarna.

## Referenser ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

