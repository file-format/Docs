---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie RM failo formatą ir API, kurios gali sukurti ir atidaryti RM failąs.
title: RM failo formaat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Kas yra RM failas? ##

RealMedia yra patentuotas daugialypės terpės konteinerio formatas, kurį sukūrė RealNetworks ir kuris naudoja plėtinį .rm. Jis naudojamas su [RealAudio (RA)](/audio/ra/) ir [RealVideo(RV)](/video/rv/) deriniu srautiniam perdavimui internetu. Šie srautai yra pastovaus pralaidumo. Kintamam bitų dažniui RealNetworks sukūrė RealMedia Variable Bitrate (RMVB) formatą. RealMedia tinka srautiniam turiniui perduoti internetu ir, pavyzdžiui, gali būti naudojama tiesioginei televizijai transliuoti.

## „RealMedia“ failo ## struktūra

RealMedia failą sudaro daugybė dalių, kurių kiekviena turi tokią struktūrą:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Toliau pateikiami RealMedia faile esančių dalių tipai:

– **RealMedia failo antraštė (.RMF)**: tai turi būti pirmoji RealMedia failo dalis. Viename faile yra tik viena RMF dalis. Jame pateikiama informacija apie antraščių skaičių.
- **Failo ypatybių antraštė (PROP)**: čia pateikiama informacija apie bendrąsias RealMedia failo ypatybes. Kiekviename RealMedia faile yra tik viena šio tipo dalis.
- **Medijos ypatybių antraštė (MDPR)**: šioje dalyje yra informacijos apie srauto ypatybes. Jame yra informacijos apie srauto tipą ir naudojamą kodeką. Kiekvienam failo srautui yra viena MDPR dalis.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Duomenų antraštė (DATA)**: šioje dalyje yra duomenų paketų grupė.
- **Indekso antraštė (INDX)**: ši dalis pateikiama po visų DUOMENŲ gabalų ir jame yra indekso įrašų. Viename faile gali būti daugiau nei viena INDX dalis.

## Palaikomi garso ir vaizdo formatai ##

### Garso formatai ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- virėjas: virėjas
- atrc: ATRAC3
- ralf: RealAudio Lossless formatas
- Raac: LC-AAC
- racp: HE-AAC

### Vaizdo įrašų formatai ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 pirmtakas
- RV40: H.264 pirmtakas, RV40
– RVTR: H.263+ (RV20)

## Nuorodos Nr.

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

