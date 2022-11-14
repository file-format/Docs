---
date: 2020-08-12
keywords: jxr, .jxr, formato di file jxr, come aprire i file jxr, estensione .jxr, estensione jxr
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file JXR
linktitle: JXR
description: "Scopri il formato di file JXR e le API che possono creare e aprire file JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Che cos'è un file JXR? ##

JPEG XR (JPEG range esteso) è un formato di file per immagini fotografiche a tono continuo. È uno standard di compressione di immagini fisse basato su HD Photo sviluppato da Microsoft. Supporta sia la compressione lossy che lossless.

## Breve storia ##

Windows Media Photo è stato annunciato per la prima volta da Microsoft a WinHEC 2006. È stato ribattezzato HD Photo nel novembre 2006. JPEG XR è stato approvato come standard internazionale ISO/IEC 29199-2 il 19 giugno 2009. ITU-T e ISO/IEC hanno pubblicato una mozione specifica del formato (ITU-T T.833 | ISO/IEC 29199-3), un set di test di conformità (ITU-T T.834 | ISO/IEC 29199-4) e un software di riferimento (ITU-T T.835 | ISO /IEC 29199-5) per JPEG XR dopo il completamento delle specifiche di codifica delle immagini nel 2010. Nel 2011 è stata pubblicata una relazione tecnica che descrive l'architettura del flusso di lavoro per JPEG XR.

## Disegno JPEG XR ##

Rispetto a JPEG, JPEG XR offre diversi miglioramenti tra cui:

- **Migliore compressione**: JPEG XR offre rapporti di compressione più elevati.
- **Compressione senza perdita di dati**: JPEG XR supporta la compressione senza perdita di dati.
- **Struttura tile**: l'immagine JPEG XR può essere segmentata in regioni tile in cui ciascuna regione può essere decodificata separatamente.
- **Maggiore precisione del colore**: JPEG XR include la conversione interna nello spazio colore YCoCg per supportare le immagini utilizzando lo spazio colore RGB. JPEG XR supporta anche un modello di colore CMYK intero a 16 bit per componente (64 bit per pixel). JPEG XR supporta il formato colore a virgola mobile a esponente condiviso RGBE per le immagini HDR. JPEG XR supporta anche le codifiche dei colori in scala di grigi e multicanale.
- **Mappa di trasparenza**: JPEG XR supporta il canale alfa per la trasparenza.
- **Modifica dell'immagine del dominio compresso**: le immagini JPEG XR possono essere convertite in una codifica con perdita di dati, ridotte in risoluzione, ritagliate, capovolte, ruotate e la struttura del riquadro può essere modificata senza decodificare completamente il file.
- **Supporto per i metadati**: il file immagine JPEG XR può contenere il profilo colore ICC per una rappresentazione del colore coerente su più dispositivi. Il formato supporta anche i formati di metadati Exif e XMP.

## Formato contenitore ##

I dati di immagine JPEG XR possono essere archiviati in un formato contenitore simile a TIFF utilizzando una tabella di tag IFT (Image File Directory). Un file JXR contiene quanto segue nei tag IFD:

- Dati immagine: sono dati immagine contigui autonomi.
- Dati canale alfa opzionali: se presenti, i dati dell'immagine possono essere compressi separatamente consentendo il supporto di applicazioni che non supportano la trasparenza.
- Metadati
- Metadati XMP opzionali
- Metadati Exif opzionali

Poiché si basa sul formato TIFF, eredita tutte le limitazioni del formato TIFF come il limite di dimensione del file di 4 GB.

## Riferimenti ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

