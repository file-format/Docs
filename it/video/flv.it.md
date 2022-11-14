---
date: 2019-10-11
keywords: flv, .flv, formato file flv, formato file .flv, estensione .flv, estensione flv, formato video flv
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file FLV e le API che possono creare e aprire file FLV."
title: Formato file FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Che cos'è un file FLV? ##

FLV (Flash Video) è un formato di file contenitore con estensione .flv. FLV viene utilizzato per fornire contenuti audio/video su Internet utilizzando Adobe Flash Player o Adobe Air. I dati nei file FLV sono codificati allo stesso modo dei file SWF. Il supporto diretto è stato aggiunto a Flash Player 7 nel 2003. I sistemi Adobe hanno creato F4V nel 2007 a causa delle restrizioni di FLV.

### Codifica ###

I file FLV contengono bitstream video di Sorenson Spark che sono una variante proprietaria dello standard video H.263. È il formato di compressione richiesto per Flash Player 6 e 7. La versione 8 di Flash Player supporta i flussi video On2 TrueMotion VP6. È il formato di compressione consigliato per Flash Player 8 e versioni successive. FLV supporta l'audio in MP3, Nellymoser Asao Codec e il codec Speex open source. Supporta anche l'audio non compresso o l'audio in formato ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile e AAC-LC) sono supportati dalle versioni recenti di Flash Player 9.

## Struttura ##

I file FLV sono costituiti da intestazione e pacchetti. Un file FLV inizia con l'intestazione. L'intestazione ha i seguenti campi.

- **Firma**: il suo valore è FLV
- **Versione**: il suo valore predefinito è 1. È valido solo 0x01.
- **Flags**: 0x04 viene utilizzato per l'audio e 0x01 viene utilizzato per il video, quindi 0x05 viene utilizzato sia per l'audio che per il video.
- **Dimensione intestazione**: il valore predefinito è 9. Viene utilizzato per saltare un'intestazione espansa più recente.

Dopo l'intestazione arrivano i pacchetti. Il file FLV è suddiviso in più pacchetti chiamati tag FLV che hanno intestazioni di 15 byte. I pacchetti contengono i metadati per audio, video, script, informazioni di crittografia e payload. I pacchetti FLV hanno i seguenti campi.

- **Riservato**: è riservato per FMS e dovrebbe essere 0.
- **Filtro**: indica se i pacchetti sono filtrati o meno.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Tipo di pacchetto**: definisce il tipo di contenuto nel pacchetto.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Dimensione dati**: indica la lunghezza del messaggio.
- **Timestamp Lower**: memorizza il timestamp in millisecondi a cui si applicano i dati del tag. È impostato su NULL per il primo pacchetto.
- **Timestamp Upper**: estensione per creare un valore uint32_be.
- **Stream ID**: è impostato su NULL per il primo stream.
- **Dati payload**: questi sono i dati basati sul tipo di pacchetto.

## Riferimenti ##

- [Video Flash - Wikipedia](https://en.wikipedia.org/wiki/Video_Flash)

