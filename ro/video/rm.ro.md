---
date: 2019-10-11
keywords: rm, .rm, format de fișier rm, format de fișier .rm, extensie .rm, format de fișier RealMedia
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier RM și despre API-urile care pot crea și deschide fișiere RM."
title: Format de fișier RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Ce este un fișier RM? ##

RealMedia este un format de container multimedia proprietar dezvoltat de RealNetworks care utilizează extensia .rm. Este folosit cu combinația de [RealAudio (RA)](/ro/audio/ra/) și [RealVideo(RV)](/ro/video/rv/) pentru streaming pe internet. Aceste fluxuri au un bitrate constant. Pentru rata de biți variabilă, RealNetworks a dezvoltat formatul RealMedia Variable Bitrate (RMVB). RealMedia este potrivit pentru streaming de conținut pe internet și poate fi folosit pentru transmiterea în direct a televiziunii, de exemplu.

## Structura fișierului RealMedia ##

Un fișier RealMedia constă dintr-o serie de bucăți, fiecare având următoarea structură:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Următoarele sunt tipurile de bucăți prezente în fișierul RealMedia:

- **Antetul fișierului RealMedia (.RMF)**: Aceasta trebuie să fie prima bucată din fișierul RealMedia. Doar o bucată RMF este prezentă într-un fișier. Conține informații despre numărul de anteturi.
- **Antetul proprietăților fișierului (PROP)**: Acesta conține informații despre proprietățile generale ale fișierului RealMedia. Există o singură bucată de acest tip în fiecare fișier RealMedia.
- **Antetul proprietăților media (MDPR)**: Această bucată conține informații despre proprietățile fluxului. Conține informații despre tipul de flux și codecul utilizat. Există o bucată MDPR pentru fiecare flux din fișier.
- **Antetul descrierii conținutului (CONT)**: această bucată conține informații text, cum ar fi titlul sau autorul conținutului din fișierul RealMedia. Această bucată are doar scop informativ.
- **Antet de date (DATE)**: Această bucată conține un grup de pachete de date.
- **Index header (INDX)**: Această bucată vine după toate bucățile DATE și conține intrări de index. Un fișier poate avea mai multe bucăți INDX.

## Formate audio și video acceptate ##

### Formate audio ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- bucătar: bucătar
- atrc: ATRAC3
- ralf: Format RealAudio Lossless
- raac: LC-AAC
- racp: HE-AAC

### Formate video ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: precursor H.264
- RV40: precursor H.264, RV40
- RVTR: H.263+ (RV20)

## Referințe ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

