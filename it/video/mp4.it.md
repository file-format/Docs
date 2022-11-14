---
date: 2019-10-11
keywords: MP4, file, estensione, formato, formato video, MPEG-4
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file MP4 e le API che possono creare e aprire file MP4."
title: Formato file MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Che cos'è un file MP4? ##

MP4 (abbreviazione di MPEG-4 Part 14) è un formato di file basato su ISO/IEC 14496-12:2004 basato su QuickTime File Format ma specifica formalmente il supporto per Initial Object Descriptor (IOD) e altre funzionalità MPEG. Viene utilizzato principalmente per archiviare video e audio, ma può anche essere utilizzato per memorizzare sottotitoli e immagini fisse. I file MP4 vengono archiviati con l'estensione .mp4. MP4 è uno standard di codifica audiovisivo internazionale. Simile ai formati contenitore più moderni, MP4 supporta lo streaming su Internet. A causa dell'elevata compressione utilizzata in MP4, i file risultanti sono di dimensioni inferiori con quasi tutta la qualità originale mantenuta.

## Breve storia ##

La specifica MP4 è stata sviluppata da Moving Picture Experts Group (MPEG) e si basava sul formato QuickTime [MOV](/it/video/mov/) pubblicato nel 2001. La prima versione (ISO/IEC 14496-1:2001) di MP4 era una revisione della specifica MPEG-4 Part 1: Systems pubblicata nel 1999. Il formato di file MP4 è stato generalizzato a ISO Base Media File Format ISO/IEC 14496-12:2004 che ha definito la struttura generale per i file multimediali basati sul tempo. Di conseguenza, viene utilizzato come base per altri formati di file.

## Struttura dei file MP4 ##

MP4 è un file contenitore estensibile, il che significa che non definisce una struttura rigida e consente una struttura e una gerarchia personalizzate per ogni tipo di supporto. I dati nel file MP4 sono divisi in due sezioni, la prima contenente i dati relativi ai media e la seconda contenente i metadati. I dati multimediali contengono audio o video e i metadati indicano flag per l'accesso casuale, timestamp, ecc.
Le strutture in MP4 sono in genere indicate come atomi o scatole. La dimensione minima di un atomo è 8 byte (i primi 4 byte specificano la dimensione e i successivi 4 byte specificano il tipo). Ecco un elenco degli atomi di livello radice contenuti nei file MP:

- **ftyp**: contiene il tipo di file, la descrizione e le strutture dati comuni utilizzate.
- **pdin**: contiene informazioni sul caricamento/scaricamento progressivo del video.
- **moov**: contenitore per tutti i metadati del film.
- **moof**: contenitore con frammenti video.
- **mfra**: il contenitore con accesso casuale al frammento video
- **mdat**: contenitore di dati per i media.
- **stts**: tabella campione-tempo.
- **stsc**: tabella da campione a pezzo.
- **stsz**: dimensioni del campione (inquadratura)
- **meta**: il contenitore con le informazioni sui metadati.

Ecco un elenco di atomi di secondo livello utilizzati in MP4:

- **mvhd**: contiene le informazioni sull'intestazione del video con tutti i dettagli del video.
- **trak**: container con il singolo binario.
- **udta**: il contenitore con l'utente e le informazioni sulla traccia.
- **iods**: descrittore di file MP4

## Riferimenti ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

