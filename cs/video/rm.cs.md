---
date: 2019-10-11
keywords: rm, .rm, formát souboru rm, formát souboru .rm, přípona .rm, formát souboru RealMedia
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru RM a rozhraních API, která mohou vytvářet a otevírat soubory RM."
title: Formát souboru RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Co je soubor RM? ##

RealMedia je proprietární formát multimediálního kontejneru vyvinutý společností RealNetworks, který používá příponu .rm. Používá se s kombinací [RealAudio (RA)](/cs/audio/ra/) a [RealVideo(RV)](/cs/video/rv/) pro streamování přes internet. Tyto toky mají konstantní datový tok. Pro variabilní datový tok vyvinul RealNetworks formát RealMedia Variable Bitrate (RMVB). RealMedia je vhodná pro streamování obsahu přes internet a lze ji použít například pro streamování živého televizního vysílání.

## Struktura souboru RealMedia ##

Soubor RealMedia se skládá z řady částí, z nichž každá má následující strukturu:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

V souboru RealMedia jsou uvedeny následující typy bloků:

- **Záhlaví souboru RealMedia (.RMF)**: Toto musí být první blok v souboru RealMedia. V jednom souboru je přítomen pouze jeden blok RMF. Obsahuje informaci o počtu hlaviček.
- **Záhlaví vlastností souboru (PROP)**: Obsahuje informace o obecných vlastnostech souboru RealMedia. V každém souboru RealMedia je pouze jeden blok tohoto typu.
- **Záhlaví vlastností médií (MDPR)**: Tento blok obsahuje informace o vlastnostech streamu. Obsahuje informace o typu streamu a použitém kodeku. Pro každý datový proud v souboru existuje jeden blok MDPR.
- **Záhlaví popisu obsahu (CONT)**: Tento blok obsahuje textové informace, jako je název nebo autor obsahu v souboru RealMedia. Tento blok je pouze pro informační účely.
- **Datové záhlaví (DATA)**: Tento blok obsahuje skupinu datových paketů.
- **Záhlaví indexu (INDX)**: Tento blok následuje po všech částech DATA a obsahuje položky indexu. Jeden soubor může mít více než jeden blok INDX.

## Podporované audio a video formáty ##

### Zvukové formáty ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- kuchař: Vařit
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Formáty videa ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: prekurzor H.264
- RV40: prekurzor H.264, RV40
- RVTR: H.263+ (RV20)

## Reference ##

- [RealMedia - Wikipedie](https://en.wikipedia.org/wiki/RealMedia)

