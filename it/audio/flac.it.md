---
date: 2019-12-13
keywords: flac, formato file flac, estensione .flac, file flac, flac vs mp3
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file FLAC e le API che possono creare e aprire file FLAC."
title: Formato file FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Che cos'è un file FLAC?

FLAC (Free Lossless Audio Codec) è un formato di codifica audio a compressione senza perdita di dati sviluppato da Xiph.Org Foundation. FLAC è un formato aperto esente da royalty che viene salvato con l'estensione .flac. L'audio digitale compresso utilizzando l'algoritmo FLAC è in genere ridotto dal 50 al 70 percento in termini di dimensioni. I file FLAC possono essere decompressi in una copia identica dei file audio originali.

## Formato file FLAC

Questa è una panoramica del flusso di bit FLAC.

- **marcatore fLaC**: questo marcatore viene aggiunto all'inizio del flusso. È seguito da uno o più blocchi di metadati.
- **Blocchi di metadati**: FLAC supporta 128 tipi di blocchi di metadati; attualmente sono definiti i seguenti.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: i dati audio sono composti da uno o più frame audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Breve storia del formato file FLAC

Josh Coalson ha iniziato lo sviluppo di FLAC nel 2000. La prima versione di FLAC è stata rilasciata il 20 luglio 2001. FLAC è stato incorporato sotto la bandiera Xiph.Org il 20 gennaio 2003. Lo sviluppo di FLAC è stato spostato nel repository git Xiph.Org con il rilascio della versione 1.3.0 il 26 marzo 2013.

## Composizione del progetto FLAC

Il progetto FLAC è composto da:

- Formati di streaming.
- Formato contenitore semplice per il flusso (FLAC).
- libFLAC: una libreria di codificatori di riferimento, decodificatori e interfaccia di metadati.
- libFLAC++: un wrapper orientato agli oggetti per libFLAC.
- flac: un programma da riga di comando per codificare e decodificare flussi FLAC.
- metaflac: un editor di metadati da riga di comando per FLAC.
- Plugin di input per lettori musicali come Winamp, XMMX, ecc.
- Formato contenitore Ogg (Ogg FLAC).

## Design FLAC

A seconda della densità e dell'ampiezza della musica, la dimensione del file compresso può essere inferiore dell'80% rispetto al file originale.

### Codificatore sorgente ###

- Supporta solo campioni interi e non in virgola mobile. Può gestire una risoluzione in bit PCM da 4 a 32 bit per campione e una frequenza di campionamento da 1 Hz a 65.535 Hz. La codifica FLAC è limitata a 24 bit per campione.
- I canali possono essere raggruppati per sfruttare le correlazioni intercanale per aumentare la compressione.
- I checksum CRC vengono utilizzati per identificare i frame danneggiati.
- Per la conversione di campioni audio, FLAC utilizza la previsione lineare.

### Metadati ###

- FLAC supporta ReplayGain (usato per percepire e normalizzare il volume dell'audio).
- FLAC utilizza lo stesso sistema utilizzato nei commenti Vorbis per i tag.
- libFLAC è utilizzato dalla maggior parte delle applicazioni FLAC per la codifica/decodifica.
- L'API libFLAC è organizzata in flussi, flussi ricercabili e file per aumentare l'astrazione dal flusso di bit FLAC di base.

### Compressione ###

libFLAC utilizza livelli di compressione da 0 a 8 dove 0 è il livello di compressione più veloce e 8 è il livello di compressione più lento. I file compressi sono sempre senza perdita di dati sebbene il compromesso sia tra velocità e dimensione.

## FLAC vs MP3
L'MP3 è un formato di compressione con perdita, il che significa che potrebbe tagliare parte dell'audio per ridurne le dimensioni dopo aver applicato la compressione. Considerando che FLAC è un formato di file senza perdita di dati, il che significa che puoi ascoltare l'audio nella sua forma più pura. In precedenza i formati di file senza perdita di dati erano CDA o WAV che non erano molto efficienti in termini di spazio come FLAC. La tabella seguente mostrerà il confronto tra questi due formati per alcuni termini importanti:

|Termine|FLAC|MP3|
---|---|---|
|**Qualità dei dati**|Nessuna perdita di dati audio| Alcuni dati potrebbero andare persi durante la compressione dei dati audio|
|**Size**|Dimensioni del file maggiori rispetto ai formati con perdita di dati. Quindi è necessaria una maggiore capacità di archiviazione | File di dimensioni inferiori, adatti per la riproduzione su dispositivi audio compatti con poco spazio di archiviazione |
|**Requisiti hardware**| Hai bisogno di apparecchiature audio di alta qualità e di un'enorme capacità di archiviazione | È possibile salvare enormi librerie audio in uno spazio di archiviazione più piccolo. Adatto per dispositivi palmari, come lettori audio o telefoni cellulari|
|**Distribuzione su Internet**|Non può essere distribuito facilmente su Internet a causa delle enormi dimensioni del file |Le dimensioni compatte del file ne facilitano la distribuzione su Internet|
|**Compatibilità**|Il codec di ascolto musicale e audio più popolare che è praticamente compatibile con tutti i dispositivi del pianetaCompatibile con PC, telefoni, ricevitori AV, lettori Blu-ray, dispositivi di streaming di nuova generazione come Roku o Fire TV|

## Riferimenti ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

