---
date: 2020-08-12
keywords: jfif, .jfif, jfif filformat, hur man öppnar jfif-filer, .jfif extension, jfif extension
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF-fil - Vad är en .jfif-fil?
linktitle: JFIF
description: "Lär dig om JFIF-filformat och API:er som kan skapa och öppna JFIF-filer." 
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Vad är JFIF fil?

JFIF (JPEG File Interchange Format (JFIF)) är en bildformatsfil som använder filtillägget .jfif. JFIF bygger över JIF (JPEG Interchange Format) genom att minska komplexiteten och lösa dess begränsningar.

## Kort historik om JFIF

JFIF-dokumentutveckling leddes av Eric Hamilton och ett avtal om den första versionen upprättades i slutet av 1991. Version 1.02 publicerades den 7 september 1992. RFC 2046 specificerade att JFIF-formatet används för att överföra JPEG-bilder över internet. JFIF publicerades av ECMA 2009 och standardiserades av ITU-T 2011 som dess rekommendation T.871 och av ISO/IEC 2013 som ISO/IEC 10918-5

## JFIF-filformat ##

En JFIF-fil består av en sekvens av markörer som definieras i del 1 av JPEG-standarden. Varje markör består av två byte (FF följt av en byte som anger typen av markör). Markörer kan antingen vara fristående eller indikera början av ett markörsegment.

JFIF tillåter flera komponenter som Y, Cb, Cr att ha olika upplösningar men deras inriktning är inte definierad. Till skillnad från JPEG kan JFIF tillhandahålla information om upplösning och bildförhållande. JFIF definierar också vilken färgmodell som ska användas.

### Filstruktur ##

|Segment|Kod|Beskrivning|
|---|---|---|
|SOI|FF D8|Start av bild|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|ytterligare markörsegment|
|SOS|FF DA|Start av skanning|
||komprimerad bilddata||
|EOI|FF D9|Slut på bild|

JFIF-standarden definierar följande segment:

### JFIF APP0 markörsegment ###

Det är ett obligatoriskt segment som innehåller bildparametrar. Den kan också innehålla en inbäddad okomprimerad miniatyrbild.

|Fält|Storlek (byte)|Beskrivning|
|---|---|---|
|APP0 markör|2|FF E0|
|Längd|2|Längd på segmentet exklusive APP0-markör|
|Identifier|5|JFIF (4A 46 49 46 00) i ASCII avslutad med en nollbyte|
|JFIF version|2|Version av JFIF|
|Densitetsenheter|1|Enhet för följande pixeldensitetsfält</br> 00 : Inga enheter; bredd:höjd pixelbildförhållande är lika med Ydensity:Xdensity</br> 01 : Pixlar per tum</br> 02 : Pixlar per centimeter|
|Xdensity|2|Horisontell pixeltäthet större än noll|
|Ydensity|2|Vertikal pixeltäthet större än noll|
|Xthumbnail|1|Horisontellt antal pixlar för den inbäddade RGB-miniatyrbilden. Kan vara noll|
|Ythumbnail|1|Vertikalt pixelantal för den inbäddade RGB-miniatyren. Kan vara noll|
|Miniatyrdata|3 × n|Okomprimerad 24-bitars RGB-rasterminiatyrdata|

### JFIF extension APP0 markörsegment ###

Detta är en valfri sektion som, om den definieras, omedelbart måste följa JFIF APP0-markörsegmentet. Det här avsnittet stöds av JFIF version 1.02 och senare och tillåter inbäddning av miniatyrer i tre olika format.

|Fält|Storlek (byte)|Beskrivning|
|---|---|---|
|APP0 markör|2|FF E0|
|Längd|2|Längd på segmentet exklusive APP0-markör|
|Identifier|5|JFXX (4A 46 58 58 00) i ASCII avslutad med en nollbyte|
|Miniatyrformat|1|Anger vilket dataformat som används för följande inbäddade miniatyr:</br> 10: JPEG-format</br> 11 : 1 byte per pixel palettformat</br> 13 : 3 byte per pixel RGB-format|
|Miniatyrdata|variabel||

## Konvertering av JFIF till andra bildfilformat

JFIF kan konverteras till populära bildfilformat som [PNG](/sv/image/png/), [JPG](/sv/image/jpg/) och [PDF](/sv/pdf/).

## Referenser ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

