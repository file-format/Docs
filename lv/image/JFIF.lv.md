---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF fails — kas ir .jfif failse?
linktitle: JFIF
description: Lnopelniet par JFIF faila formātu un API, kas var izveidot un atvērt JFIF failus.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Kas ir JFIF fails?

JFIF (JPEG failu apmaiņas formāts (JFIF)) ir attēla formāta fails, kurā tiek izmantots paplašinājums .jfif. JFIF tiek veidots, izmantojot JIF (JPEG apmaiņas formātu), samazinot sarežģītību un novēršot tā ierobežojumus.

## Īsa JFIF vēsture

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. Versija 1.02 tika publicēta 1992. gada 7. septembrī. RFC 2046 norādīja, ka JPEG attēlu pārsūtīšanai internetā tiek izmantots JFIF formāts. JFIF publicēja ECMA 2009. gadā, un ITU-T to standartizēja 2011. gadā kā savu ieteikumu T.871 un ISO/IEC 2013. gadā kā ISO/IEC 10918-5.

## JFIF faila formāts ##

JFIF fails sastāv no marķieru secības, kā noteikts JPEG standarta 1. daļā. Katrs marķieris sastāv no diviem baitiem (FF, kam seko baits, kas norāda marķiera veidu). Marķieri var būt atsevišķi vai norādīt marķiera segmenta sākumu.

JFIF ļauj vairākiem komponentiem, piemēram, Y, Cb, Cr, būt ar dažādu izšķirtspēju, taču to izlīdzināšana nav noteikta. Atšķirībā no JPEG, JFIF var nodrošināt informāciju par izšķirtspēju un malu attiecību. JFIF nosaka arī izmantojamo krāsu modeli.

### Faila struktūra ##

|Segments|Kods|Apraksts|
|---|---|---|
|SOI|FF D8|Attēla sākums|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|papildu marķieru segmenti|
|SOS|FF DA|Skenēšanas sākums|
||saspiesti attēla dati||
|EOI|FF D9|Attēla beigas|

JFIF standarts nosaka šādus segmentus:

### JFIF APP0 marķiera segments ###

Tas ir obligāts segments, kas satur attēla parametrus. Tajā var būt arī iegults nesaspiests sīktēls.

|Lauks|Izmērs (baiti)|Apraksts|
|---|---|---|
|APP0 marķieris|2|FF E0|
|Length|2|Segmenta garums, izņemot APP0 marķieri|
|Identifier|5|JFIF (4A 46 49 46 00) ASCII beidzas ar nulles baitu|
|JFIF versija|2|JFIF versija|
|Blīvuma vienības|1|Mērvienība šādiem pikseļu blīvuma laukiem</br> 00 : nav vienību; platuma:augstuma pikseļu malu attiecība ir vienāda ar Ydensity:Xdensity</br> 01: pikseļi collā</br> 02 : pikseļi uz centimetru|
|Xdensity|2|Horizontālais pikseļu blīvums lielāks par nulli|
|Idensity|2|Vertikālais pikseļu blīvums lielāks par nulli|
|Xthumbnail|1|Iegultā RGB sīktēla horizontālais pikseļu skaits. Var būt nulle|
|Ythumbnail|1|Iegultā RGB sīktēla vertikālais pikseļu skaits. Var būt nulle|
|Sīktēlu dati|3 × n|Nesaspiesti 24 bitu RGB rastra sīktēlu dati|

### JFIF paplašinājuma APP0 marķiera segments ###

Šī ir izvēles sadaļa, kurai, ja tā ir noteikta, nekavējoties jāseko JFIF APP0 marķiera segmentam. Šo sadaļu atbalsta JFIF versija 1.02 un jaunāka versija, un tā ļauj iegult sīktēlus trīs dažādos formātos.

|Lauks|Izmērs (baiti)|Apraksts|
|---|---|---|
|APP0 marķieris|2|FF E0|
|Length|2|Segmenta garums, izņemot APP0 marķieri|
|Identifier|5|JFXX (4A 46 58 58 00) ASCII beidzas ar nulles baitu|
|Sīktēla formāts|1|Norāda, kāds datu formāts tiek izmantots šim iegultajam sīktēlam:</br> 10: JPEG formāts</br> 11: 1 baits uz vienu pikseļu paletē formātā</br> 13 : 3 baiti uz pikseļu RGB formāts|
|Sīktēlu dati|mainīgais||

## JFIF konvertēšana uz citiem attēlu failu formātiem

JFIF var pārvērst populāros attēlu failu formātos, piemēram, [PNG](/image/png/), [JPG](/image/jpeg/) un [PDF](/pdf/).

## Atsauces Nr.

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

