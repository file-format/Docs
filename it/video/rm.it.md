---
date: 2019-10-11
keywords: rm, .rm, formato file rm, formato file .rm, estensione .rm, formato file RealMedia
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file RM e le API che possono creare e aprire file RM."
title: Formato file RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Che cos'è un file RM? ##

RealMedia è un formato contenitore multimediale proprietario sviluppato da RealNetworks che utilizza l'estensione .rm. Viene utilizzato con la combinazione di [RealAudio (RA)](/it/audio/ra/) e [RealVideo(RV)](/it/video/rv/) per lo streaming su Internet. Questi flussi hanno un bitrate costante. Per il bitrate variabile, RealNetworks ha sviluppato il formato RealMedia Variable Bitrate (RMVB). RealMedia è adatto per lo streaming di contenuti su Internet e può essere utilizzato, ad esempio, per lo streaming di programmi televisivi in diretta.

## Struttura del file RealMedia ##

Un file RealMedia è costituito da una serie di blocchi, ciascuno con la seguente struttura:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Di seguito sono riportati i tipi di blocchi presenti nel file RealMedia:

- **Intestazione del file RealMedia (.RMF)**: questo deve essere il primo blocco nel file RealMedia. In un file è presente solo un blocco RMF. Contiene informazioni sul numero di intestazioni.
- **Intestazione delle proprietà del file (PROP)**: contiene informazioni sulle proprietà generali del file RealMedia. C'è solo un pezzo di questo tipo in ogni file RealMedia.
- **Intestazione delle proprietà multimediali (MDPR)**: questo blocco contiene informazioni sulle proprietà del flusso. Contiene informazioni sul tipo di flusso e sul codec utilizzato. C'è un blocco MDPR per ogni flusso nel file.
- **Intestazione della descrizione del contenuto (CONT)**: questo blocco contiene informazioni di testo come il titolo o l'autore del contenuto nel file RealMedia. Questo pezzo è solo a scopo informativo.
- **Intestazione dati (DATA)**: questo blocco contiene un gruppo di pacchetti di dati.
- **Intestazione dell'indice (INDX)**: questo blocco viene dopo tutti i blocchi DATI e contiene le voci dell'indice. Un file può avere più di un blocco INDX.

## Formati audio e video supportati ##

### Formati audio ###

-lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- rete: AC3
- sipr: Sipro
- cucinare: cucinare
- atrc: ATRAC3
- ralf: formato RealAudio Lossless
- raac: LC-AAC
- gara: HE-AAC

### Formati video ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: precursore H.264
- RV40: precursore H.264, RV40
- RVTR: H.263+ (RV20)

## Riferimenti ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

