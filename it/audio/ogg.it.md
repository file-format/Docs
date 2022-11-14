---
date: 2019-12-13
keywords: ogg, formato file ogg, estensione .ogg, formato audio ogg
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file OGG e le API che possono creare e aprire file OGG."
title: File OGG - File audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Che cos'è un file OGG?

OGG è un file audio compresso Ogg Vorbis che viene salvato con l'estensione .ogg. I file OGG vengono utilizzati per archiviare dati audio e possono includere anche informazioni e metadati sull'artista e sulla traccia. OGG è un formato contenitore gratuito e aperto gestito da Xiph.Org Foundation.

## Breve storia del formato di file OGG

Il progetto Ogg è iniziato come parte di un progetto più ampio nel 1993 ed è stato chiamato Squish ma a causa di un marchio esistente, è stato ribattezzato OggSquish. È stato descritto come un tentativo di creare un formato audio compresso flessibile per le moderne applicazioni audio. Il riferimento OGG è stato separato da Vorbis il 2 settembre 2000.

OGM è stato creato nel 2002 a causa della mancanza di supporto video formale in OGG. Ciò ha consentito di incorporare video dal framework Microsoft DirectShow in un wrapper basato su OGG. Nel 2006, OGG era supportato da molti motori di videogiochi ed era comunemente usato per codificare contenuti gratuiti. La Free Software Foundation ha avviato una campagna il 15 maggio 2007 per aumentare l'uso di Vorbis come alternativa superiore all'MP3. Entro il 30 giugno 2009, OGG era l'unico formato contenitore supportato dall'implementazione HTML5 di Firefox 3.5.

## Formato file OGG

Il formato OGG è costituito da blocchi di dati. Ogni pezzo è chiamato pagina Ogg. Ogni pagina inizia con "OggS" per identificare il formato Ogg. L'intestazione contiene il numero di serie e il numero di pagina che identifica ogni pagina come parte di una serie. La pagina è composta dai seguenti componenti.

- **Intestazione di pagina**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| bit | Valore | Descrizione |
| --- | --- | --- |
| 0 | 0x01 | Indica che il primo pacchetto della pagina è la continuazione del pacchetto precedente nel flusso di bit logico. |
| 1 | 0x02 | Indica che questa pagina è la prima nel flusso di bit logico. |
| 2 | 0x04 | Indica che questa pagina è l'ultima nel flusso di bit logico. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadati**: VorbisComment è il meccanismo più ampiamente supportato per l'archiviazione dei metadati. Altri meccanismi includono quanto segue:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Riferimenti ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

