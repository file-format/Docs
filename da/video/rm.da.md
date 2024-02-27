---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om RM filformat og API'er, der kan oprette og åbne RM fils.
title: RM fil formularat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Hvad er en RM fil? ##

RealMedia er et proprietært multimediebeholderformat udviklet af RealNetworks, der bruger .rm-udvidelsen. Den bruges sammen med kombinationen af [RealAudio (RA)](/audio/ra/) og [RealVideo(RV)](/video/rv/) til streaming over internettet. Disse strømme har konstant bithastighed. Til variabel bitrate udviklede RealNetworks RealMedia Variable Bitrate (RMVB)-formatet. RealMedia er velegnet til streaming af indhold over internettet og kan f.eks. bruges til at streame live-tv.

## Struktur af RealMedia-fil ##

En RealMedia-fil består af en række bidder, der hver har følgende struktur:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Følgende er de typer bidder, der findes i RealMedia-filen:

- **RealMedia filoverskrift (.RMF)**: Dette skal være den første del af RealMedia-filen. Kun én RMF-chunk er til stede i én fil. Den indeholder oplysninger om antallet af overskrifter.
- **Filegenskabsoverskrift (PROP)**: Dette indeholder oplysninger om de generelle egenskaber for RealMedia-filen. Der er kun én del af denne type i hver RealMedia-fil.
- **Medieegenskaber-header (MDPR)**: Denne del indeholder oplysninger om streamegenskaberne. Den indeholder oplysninger om typen af stream og det anvendte codec. Der er en MDPR-chunk for hver stream i filen.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Data header (DATA)**: Denne del indeholder en gruppe af datapakker.
- **Indeksoverskrift (INDX)**: Denne chunk kommer efter alle DATA chunks og indeholder indeksposter. Én fil kan have mere end én INDX-chunks.

## Understøttede lyd- og videoformater ##

### Lydformater ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- kok: Kok
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Videoformater ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264-forløber
- RV40: H.264 precursor, RV40
- RVTR: H.263+ (RV20)

## Referencer ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

