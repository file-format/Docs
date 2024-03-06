---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lnopelniet par WEBM faila formātu un API, kas var izveidot un atvērt WEBM failus.
title: WEBM — WebM video faila veidlapaat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Kas ir WEBM fails?

Fails ar paplašinājumu .webm ir video fails, kura pamatā ir atvērts bezatlīdzības WebM faila formāts. Tas ir paredzēts video koplietošanai tīmeklī un nosaka failu konteinera struktūru, tostarp video un audio formātus. WebM ir 100% bezmaksas, ieviešot augstas kvalitātes, pamatojoties uz atvērtām tehnoloģijām, piemēram, HTML, HTTP un TCP/IP, kuras var ieviest ikviens. WebM ir īpaši izstrādāts video rādīšanai tīmeklī, kas padara to optimizētu straumēšanai ar zemu skaitļošanas nospiedumu. Tas padara to piemērotu videoklipu atskaņošanai jebkurā ierīcē, īpaši mazjaudas netbook datoros, plaukstdatoros un planšetdatoros.

## WEBM faila formāts

WebM faila struktūra ir balstīta uz Matroska [MKV](/video/mkv/) konteinera faila formāta apakškopu. WebM failā pieejamās video straumes tiek saspiestas, izmantojot VP8 vai VP9 saspiešanas tehnoloģijas, kas ir ļoti efektīvas. Līdzīgi WebM faila audio straumes tiek saspiestas, izmantojot Vorbis vai Opus kodekus, ko izstrādāja [Xiph Foundation](https://www.xiph.org/). Visi šie video un audio kodeki ir bez autoratlīdzības, un tos var izmantot bez maksas.

Tālāk ir sniegtas WebM faila formāta specifikācijas.

|Lauks|Apraksts|
---|---|
|MIME tipa |video/webm|
|Tikai audio MIME tipa |audio/webm|
|Vienots tipa identifikators| org.webmproject.webm|
|Video kodeka nosaukums| VP8 vai VP9|
|Audio kodeka nosaukums| Vorbis vai Opus|

### WebM elementi

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Nosaukums |Apraksts|
---|---|
|EBML|Iestatiet datu EBML raksturlielumus, kas jāievēro. Katrs EBML dokuments ir jāsākas ar šo.|
|EBMLVersion |Faila izveidei izmantotā EBML parsētāja versija.|
|EBMLReadVersion|Minimālā EBML versija, kas parsētājam ir jāatbalsta, lai lasītu šo failu.|
|EBMLMaxIDLength |Maksimālais ID garums, ko atradīsit šajā failā (Matroskā — 4 vai mazāk).|
|EBMLMaxSizeLength|Maksimālais izmēru garums, ko atradīsit šajā failā (8 vai mazāk Matroskā). Tas neaizstāj elementa sākumā norādīto elementa izmēru. Elementi, kuru norādītais izmērs ir lielāks par EBMLMaxSizeLength atļauto, tiek uzskatīti par nederīgiem.|
|DocType|Virkne, kas apraksta dokumenta veidu, kas seko šai EBML galvenei (mūsu gadījumā webm).|
|DocTypeVersion|DocType tulka versija, kas izmantota, lai izveidotu failu.|
|DocTypeReadVersion|Minimālā DocType versija, kas tulkam ir jāatbalsta, lai lasītu šo failu.|

#### Globālie elementi

Pašlaik tiek atbalstīts tikai elements Vidums, kas tiek izmantots bojātu datu anulēšanai, lai izvairītos no neparedzētām darbībām, izmantojot bojātus datus. Saturs tiek izmests. Izmanto arī, lai rezervētu vietu apakšelementā vēlākai lietošanai.

#### Segments
Šis elements satur visus citus augstākā līmeņa (1. līmeņa) elementus. Parasti Matroska fails sastāv no 1 segmenta.

#### Meta meklēt informāciju

Tiek atbalstīta šāda informācijas meklēšana.

|Elementa nosaukums |Apraksts|
---|---|
|SeekHead |Ietver cita 1. līmeņa elementa pozīciju.|
|Seek |Satur vienu meklēšanas ierakstu EBML elementā.|
|SeekID |Binārais ID, kas atbilst elementa nosaukumam.|
|SeekPosition |Elementa pozīcija segmentā oktetos (0 = pirmā līmeņa 1 elements).|

## Atsauces

* [WebM](https://www.webmproject.org/)

* [WebM kodu krātuves](https://www.webmproject.org/code/#webp-repositories)


