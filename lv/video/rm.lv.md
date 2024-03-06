---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par RM faila formātu un API, kas var izveidot un atvērt RM failus.
title: RM faila veidlapaat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Kas ir RM fails? ##

RealMedia ir patentēts multivides konteinera formāts, ko izstrādājis RealNetworks un kas izmanto paplašinājumu .rm. To izmanto kopā ar [RealAudio (RA)](/audio/ra/) un [RealVideo(RV)](/video/rv/) straumēšanai internetā. Šīm straumēm ir nemainīgs bitu pārraides ātrums. Mainīgam bitu pārraides ātrumam RealNetworks izstrādāja RealMedia mainīgā bitu pārraides ātruma (RMVB) formātu. RealMedia ir piemērota satura straumēšanai internetā, un to var izmantot, piemēram, televīzijas tiešraides straumēšanai.

## RealMedia faila ## struktūra

RealMedia fails sastāv no vairākām daļām, katrai no kurām ir šāda struktūra:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Tālāk ir norādīti RealMedia failā esošo gabalu veidi.

- **RealMedia faila galvene (.RMF)**: tai ir jābūt pirmajai daļai RealMedia failā. Vienā failā ir tikai viens RMF gabals. Tajā ir informācija par virsrakstu skaitu.
- **Faila rekvizītu galvene (PROP)**: tajā ir informācija par RealMedia faila vispārīgajiem rekvizītiem. Katrā RealMedia failā ir tikai viena šāda veida daļa.
- **Multivides rekvizītu galvene (MDPR)**: šajā daļā ir informācija par straumes rekvizītiem. Tajā ir informācija par straumes veidu un izmantoto kodeku. Katrai faila straumei ir viens MDPR gabals.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Datu galvene (DATA)**: šajā daļā ir datu pakešu grupa.
- **Indeksa galvene (INDX)**: šī daļa nāk pēc visiem DATU gabaliem, un tajā ir indeksa ieraksti. Vienam failam var būt vairāk nekā viens INDX gabals.

## Atbalstītie audio un video formāti ##

### Audio formāti ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- pavārs: pavārs
- atrc: ATRAC3
- ralf: RealAudio Lossless formāts
- Raac: LC-AAC
- racp: HE-AAC

### Video formāti ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 prekursors
- RV40: H.264 prekursors, RV40
- RVTR: H.263+ (RV20)

## Atsauces Nr.

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

