---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lthuilleamh faoi fhormáid comhaid RM agus APIs ar féidir leo comhad RM a chruthú agus a oscailts.
title: RM Foirm Chomhaidat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Cad is comhad RM ann? ##

Is formáid coimeádán ilmheán dílseánaigh é RealMedia arna fhorbairt ag RealNetworks a úsáideann an síneadh .rm. Úsáidtear é leis an meascán de [RealAudio (RA)](/audio/ra/) agus [RealVideo(RV)](/video/rv/) chun sruthú thar an Idirlíon. Tá na sruthanna giotán seasta. Maidir le ráta inathraithe giotán, d'fhorbair RealNetworks an fhormáid RealMedia Athróg Giotán (RMVB). Tá RealMedia oiriúnach chun ábhar a shruthú thar an idirlíon agus is féidir é a úsáid chun teilifís bheo a shruthú mar shampla.

## Struchtúr an Chomhaid RealMedia ##

Tá sraith smután i gcomhad RealMedia, agus an struchtúr seo a leanas ag gach ceann díobh:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Seo a leanas na cineálacha smután atá i gcomhad RealMedia:

- **Ceanntásc comhaid RealMedia (.RMF)**: Caithfidh gurb é seo an chéad smután sa chomhad RealMedia. Níl ach smután RMF amháin i láthair i gcomhad amháin. Tá faisnéis ann faoi líon na gceanntásca.
- **Ceanntásc airíonna comhaid (PROP)**: Tá faisnéis ann faoi airíonna ginearálta an chomhaid RealMedia. Níl ach smután amháin den chineál seo i ngach comhad RealMedia.
- **Ceanntásc airíonna meán (MDPR)**: Tá faisnéis sa smután seo faoi airíonna an tsrutha. Tá faisnéis ann faoin gcineál srutha agus faoin gcód a úsáidtear. Tá smután MDPR amháin do gach sruth sa chomhad.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Ceanntásc sonraí (SONRAÍ)**: Tá grúpa paicéid sonraí sa smután seo.
- **Ceanntásc innéacs (INDX)**: Tagann an smután seo tar éis na smután SONRAÍ go léir agus tá iontrálacha innéacs ann. Féadfaidh níos mó ná smután INDX amháin a bheith i gcomhad amháin.

## Formáidí fuaime agus físe tacaithe ##

### Formáidí fuaime ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- cócaire: Cook
- áirc: ATRAC3
- ralf: Formáid RealAudio Lossless
- raac: LC-AAC
- racp: HE-AAC

### Formáidí físeáin ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: réamhtheachtaí H.264
- RV40: réamhtheachtaí H.264, RV40
- RVTR: H.263+ (RV20)

## Tagairtí ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

