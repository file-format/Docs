---
date: 2019-10-11
keywords: rm, .rm, rm-bestandsindeling, .rm-bestandsindeling, .rm-extensie, RealMedia-bestandsindeling
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over RM-bestandsindelingen en API's die RM-bestanden kunnen maken en openen."
title: RM-bestandsindeling
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Wat is een RM-bestand? ##

RealMedia is een eigen multimedia-containerformaat ontwikkeld door RealNetworks dat de .rm-extensie gebruikt. Het wordt gebruikt met de combinatie van [RealAudio (RA)](/nl/audio/ra/) en [RealVideo(RV)](/nl/video/rv/) voor streaming via internet. Deze streams hebben een constante bitrate. Voor variabele bitrate heeft RealNetworks het RealMedia Variable Bitrate-formaat (RMVB) ontwikkeld. RealMedia is geschikt voor het streamen van content via internet en kan bijvoorbeeld worden gebruikt voor het streamen van live televisie.

## Structuur van RealMedia-bestand ##

Een RealMedia-bestand bestaat uit een reeks chunks, elk met de volgende structuur:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Hieronder volgen de typen chunks die aanwezig zijn in het RealMedia-bestand:

- **RealMedia-bestandsheader (.RMF)**: dit moet de eerste chunk in het RealMedia-bestand zijn. Er is slechts één RMF-chunk aanwezig in één bestand. Het bevat informatie over het aantal headers.
- **Bestandseigenschappen header (PROP)**: dit bevat informatie over de algemene eigenschappen van het RealMedia-bestand. Er is slechts één stuk van dit type in elk RealMedia-bestand.
- **Media-eigenschappen header (MDPR)**: dit blok bevat informatie over de stream-eigenschappen. Het bevat informatie over het type stream en de gebruikte codec. Er is één MDPR-chunk voor elke stream in het bestand.
- **Content description header (CONT)**: dit blok bevat tekstinformatie zoals de titel of auteur van de content in het RealMedia-bestand. Dit stuk is alleen voor informatieve doeleinden.
- **Dataheader (DATA)**: dit blok bevat een groep datapakketten.
- **Indexkop (INDX)**: deze brok komt na alle DATA-blokken en bevat indexitems. Eén bestand kan meer dan één INDX-chunks hebben.

## Ondersteunde audio- en videoformaten ##

### Audioformaten ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- kok: kok
- atrc: ATRAC3
- ralf: RealAudio Lossless-formaat
- Raac: LC-AAC
- rek: HE-AAC

### Videoformaten ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264-voorloper
- RV40: H.264-voorloper, RV40
-RVTR: H.263+ (RV20)

## Referenties ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

