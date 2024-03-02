---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid ALAC agus APIs ar féidir leo comhad ALAC a chruthú agus a oscailts.
title: ALAC - Apple Lossless Fuaime Codec Foirm Comhadat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Cad is comhad ALAC ann?

Is formáid comhaid ALAC é Apple Lossless Audio Codec (ALAC) a úsáideann an coimeádán QuickTime comhlíontach MPEG-4. Tugadh isteach é i 2004 mar fhormáid comhaid dílseánaigh, go dtí 2011 nuair a chuir Apple ar fáil foinse oscailte agus saor ó ríchíosa é. Tá an fhormáid cosúil leis an [FLAC](/audio/flac/) (Codc Fuaime Gan Chailliúint Saor in Aisce) ach cuireann sé níos mó comhbhrú ar fáil i gcomparáid lena chéile. Cuireann sé rogha fuaime níos fearr ar fáil seachas [AAC](/audio/aac/) nó [MP3](/audio/mp3/). Is féidir comhaid fuaime atá ionchódaithe le CODEC ALAC a oscailt trí úsáid a bhaint as Apple QuickTime, Apple iTunes agus Micrsoft Windows Media Player le codec K-Lite.

## Formáid Comhaid ALAC

Is comhaid dhénártha iad comhaid atá bunaithe ar chód ALAC atá ar fáil mar [open source on GitHub](https://github.com/macosforge/alac) mar thagairt don fhorbróir. Tá na foinsí ann don ionchódóir agus don díchódóir ALAC. Tá áirgiúlacht líne ordaithe curtha ar fáil ag Apple freisin, ar a dtugtar `alacconvert`, chun na sonraí fuaime a léamh agus a scríobh chuig/ó Core Audio Formáid (CAF) agus [WAVE](/audio/wav/) comhaid. Seo a leanas roinnt príomhphointí maidir le formáid comhaid ALAC.

 1. `Doimhneacht Giotán` - 16, 20, 24 agus 32 giotán.
 1. `Ráta Samplach` - Aon ráta samplach slánuimhir treallach ó 1 go 384,000 Hz. D’fhéadfaí tacú le rátaí teoiriciúla suas le 4,294,967,295 (2^32 - 1) Hz.
 1. `Méid an Phaicéid' - Réamhshocrú méid an phacéid réamhshocraithe go 4096 fráma samplach fuaime in aghaidh an phaicéid. Is cinnte gur féidir méideanna paicéid eile. Mar sin féin, ní ráthaítear go n-oibreoidh méideanna paicéid neamh-mhainneachtana i gceart ar gach feiste crua-earraí a thacaíonn le Apple Lossless. Ní thacaítear le paicéid os cionn 16,384 fráma samplach.
 1. `Cainéil Tacaithe` - Tacaíonn sé le cainéal amháin go hocht. Tá an t-ord faisnéise seo a leanas ag gach cainéal.

|Num Chan| Ordú|
|---|---|
|1 | mona|
|2 | steirió (Ar chlé, ar dheis) |
|3 |MPEG 3.0 B (Lár, ar chlé, ar dheis) |
|4 |MPEG 4.0 B (Lár, Ar Chlé, Ar Dheis, Timpeall Lár)|
|5 |MPEG 5.0 D (Lár, Ar Chlé, Ar Dheas, Timpeall Chlé, Timpeall Ar Dheis)|
|6 |MPEG 5.1 D (Lár, Ar Chlé, Ar Dheas, Timpeall Chlé, Timpeall Ar Dheis, Éifeachtaí Ísealmhinicíochta)|
|7 |Apple AAC 6.1 (Lár, Ar Chlé, Ar Dheas, Timpeall Chlé, Timpeall Ar Dheis, Timpeall Lárnach, Éifeachtaí Ísealmhinicíochta)|
|8 |MPEG 7.1 B (Lár, Lár Clé, Lárionad Ar Dheis, Ar Chlé, Ar Dheas, Timpeall Ar Chlé, Timpeall Ar Dheis, Éifeachtaí Ísealmhinicíochta)|

## Tagairtí

* [ALAC - Vicipéid](https://ga.wikipedia.org/wiki/Apple_Lossless)

* [Codc Fuaime Apple Lossless](https://macosforge.github.io/alac/)

* [macosforge - alac ar GitHub](https://github.com/macosforge/alac)


