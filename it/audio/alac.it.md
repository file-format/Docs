---
date: 2021-03-21
keywords: alac, formato file alac, estensione .alac
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Scopri il formato di file ALAC e le API che possono creare e aprire file ALAC."
title: ALAC - Formato file codec audio senza perdita di dati Apple
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Che cos'è un file ALAC?

Il formato di file ALAC è Apple Lossless Audio Codec (ALAC) che utilizza il contenitore QuickTime compatibile con MPEG-4. È stato introdotto nel 2004 come formato di file proprietario, fino al 2011 quando Apple lo ha reso disponibile open source e royalty-free. Il formato è simile a [FLAC](/it/audio/flac/) (Free Lossless Audio Codec) ma offre una maggiore compressione in confronto. Offre un'alternativa dal suono migliore a [AAC](/it/audio/aac/) o [MP3](/it/audio/mp3/). I file audio codificati con codec ALAC possono essere aperti utilizzando Apple QuickTime, Apple iTunes e Micrsoft Windows Media Player con codec K-Lite.

## Formato file ALAC

I file basati sul codec ALAC sono file binari disponibili come [open source su GitHub](https://github.com/macosforge/alac) come riferimento per gli sviluppatori. Contiene le sorgenti per l'encoder e il decoder ALAC. Apple ha anche fornito un'utilità da riga di comando, chiamata `alacconvert`, per leggere e scrivere i dati audio in/da file Core Audio Format (CAF) e [WAVE](/it/audio/wav/). Di seguito sono riportati alcuni punti chiave sul formato di file ALAC.

1. "Profondità di bit" - 16, 20, 24 e 32 bit.
1. "Frequenza di campionamento" - Qualsiasi frequenza di campionamento intera arbitraria da 1 a 384.000 Hz. Possono essere supportate velocità teoriche fino a 4.294.967.295 (2^32 - 1) Hz.
1. `Dimensione pacchetto` - La dimensione predefinita del pacchetto è di 4096 fotogrammi campione di audio per pacchetto. Sono certamente possibili altre dimensioni dei pacchetti. Tuttavia, non è garantito che le dimensioni dei pacchetti non predefinite funzionino correttamente su tutti i dispositivi hardware che supportano Apple Lossless. I pacchetti superiori a 16.384 frame di esempio non sono supportati.
1. `Canali supportati` - Supporta da uno a otto canali. Ciascun canale ha il seguente ordine di informazioni.

|Numero Chan| Ordina|
|---|---|
|1 |mono|
|2 |stereo (sinistra, destra)|
|3 |MPEG 3.0 B (centro, sinistra, destra)|
|4 |MPEG 4.0 B (centro, sinistra, destra, surround centrale)|
|5 |MPEG 5.0 D (centro, sinistro, destro, surround sinistro, surround destro)|
|6 |MPEG 5.1 D (effetti centrali, sinistro, destro, surround sinistro, surround destro, bassa frequenza)|
|7 |Apple AAC 6.1 (effetti centrale, sinistro, destro, surround sinistro, surround destro, surround centrale, bassa frequenza)|
|8 |MPEG 7.1 B (Centro, Centro sinistro, Centro destro, Sinistra, Destra, Surround sinistro, Surround destro, Effetti a bassa frequenza)|

## Riferimenti

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac su GitHub](https://github.com/macosforge/alac)

