---
date: 2020-08-12
keywords: flif, .flif, formato file flif, come aprire file flif, estensione .flif, estensione flif
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file FLIF
linktitle: FLIF
description: "Scopri il formato di file FLIF e le API che possono creare e aprire file FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Che cos'è un file FLIF? ##

FLIF (Free Lossless Image Format) è un formato di immagine senza perdita di dati che utilizza l'estensione .flif per i suoi file. FLIF afferma di superare [PNG](/it/image/png/), [WebP](/it/image/webp/) senza perdita di dati, BPG senza perdita e JPEG 2000 senza perdita di dati in termini di rapporto di compressione. FLIF utilizza l'interlacciamento progressivo, grazie al quale qualsiasi download parziale dell'immagine può essere utilizzato come codifica con perdita di dati per l'intera immagine.

## Breve storia ##

FLIF è stato annunciato a settembre 2015 e la versione alfa è stata rilasciata a ottobre 2015. A settembre 2016 è stata rilasciata la prima versione stabile di FLIF.

## Design FLIF ##

FLIF utilizza una variante di CABAC (Context-adaptive binary arithmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) per la compressione. MANIAC è un algoritmo di codifica entropica sviluppato da Jon Sneyers e Pieter Wuille. In MANIAC, i contesti sono nodi di alberi decisionali che vengono appresi al momento della codifica in modo dinamico. Ciò rende il modello di contesto più specifico dell'immagine e si traduce in una migliore compressione. FLIF ha le seguenti caratteristiche:

- Supporta la compressione senza perdita di dati
- Supporta la compressione con perdita con la preelaborazione dell'encoder
- Supporta scala di grigi, RGB e RGBA
- Supporta una profondità di colore da 1 a 16 bit per canale
- Supporta file interlacciati e non interlacciati
- Supporta la decodifica progressiva di file parzialmente scaricati
- Supporta le animazioni
- Supporta i profili colore ICC incorporati, i metadati Exif e XMP
- Ha un supporto limitato per la compressione di file raw da fotocamera (RGGB)

## Formato file FLIF ##

Un file FLIF ha le seguenti quattro parti:

## Intestazione principale ##

L'intestazione principale contiene i metadati principali inclusi larghezza, altezza, profondità del colore, numero di fotogrammi.

|Tipo|Valore|Descrizione|
|---|---|---|
|4 byte|"FLIF"|Magia|
|4 bit|3 = ni ancora; 4 = io ancora; 5 = niente anima; 6 = i anim|Interlacciamento, animazione|
|4 bit|1 = Scala di grigi; 3 = RGB; 4 = RGBA|Numero di canali (nb_channels)|
|1 byte|'0','1','2' ('0'=personalizzato)|Byte per canale (Bpc)|
|variante|larghezza-1|larghezza|
|variante|altezza-1|Altezza|
|varint|nb_frames-2 (solo se animazione)|Numero di frame (nb_frames)|

## Blocchi di metadati ##

Questa parte contiene metadati non pixel come Exif/XMP, profilo colore ICC, ecc. codificati utilizzando la compressione DEFLATE. Questi blocchi sono definiti in modo simile ai blocchi PNG con la differenza che la dimensione del mandrino è codificata con un numero variabile di byte. I nomi dei blocchi possono essere di 4 lettere (4 byte) o un valore inferiore a 32 che indica un blocco non opzionale.

Quello che segue è un esempio di mandrini opzionali:

|Nome pezzo|Descrizione|Contenuto (dopo la decompressione DEFLATE)|
|---|---|---|
|iCCP|Profilo colore ICC|dati profilo colore ICC grezzo|
|eXif|Metadati Exif|Intestazione "Exif\0\0" seguita da un'intestazione TIFF e dai dati EXIF|
|eXmp|Metadati XMP|XMP contenuto in un xpacket di sola lettura senza riempimento|

### Convenzione di denominazione ###

- **Prima lettera**: le lettere maiuscole vengono utilizzate per i blocchi critici e le minuscole per i blocchi non critici.
- **Seconda lettera**: le lettere maiuscole vengono utilizzate per i blocchi pubblici e le minuscole per i blocchi privati
- **Terza lettera**: le lettere maiuscole vengono utilizzate per i mandrini necessari per visualizzare l'immagine correttamente e le lettere minuscole non sono importanti per visualizzare l'immagine.
- **Quarta lettera**: le lettere maiuscole vengono utilizzate per i mandrini che possono essere copiati alla cieca in sicurezza. I mandrini minuscoli dipendono dai dati dell'immagine.

## Seconda intestazione ##

Contiene le informazioni relative alla codifica effettiva dei pixel.

|Tipo|Descrizione|Condizione|Valore predefinito|
|---|---|---|---|
|1 byte|Byte NUL (0x00), nome del blocco di un flusso di bit FLIF16||
|uni_int(1,16)|Bit per pixel dei canali|Bpc == '0': repeat(nb_channels)|8 se Bpc == '1', 16 se Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Numero di loop|nb_frame > 1||
|uni_int(0,60_000)|Ritardo frame in ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Segnala: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|ha_custom_cutoff_and_alpha|2|
|uni_int(2,128)|divisore alfa|ha_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Flag: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Cagna|ha_bitchance_personalizzata||
|variabile|Trasformazioni (vedi sotto)|||
|uni_int(1) = 0|Bit indicatore: fatto con le trasformazioni|||
|uni_int(0,2)|Predittore pixel invisibile|alpha_zero && interlacciato && l'intervallo alfa include zero||

**Canali**

|Numero del canale|Descrizione|
|---|----|
|0|Rosso o grigio|
|1|Verde|
|2|Blu|
|3|Alfa|

**Trasformazioni**

|Tipo|Descrizione|
|---|---|
|uni_int(1) = 1|Bit indicatore: non ancora completato|
|uni_int(0,13)|Identificatore di trasformazione|
|variabile|Dati di trasformazione (dipende dalla trasformazione)|

La trasformazione viene utilizzata per modificare i dati dei pixel per una migliore compressione e per tenere traccia dei valori dei pixel effettivi.

## Dati pixel ##

Questa parte contiene i dati dei pixel effettivi codificati utilizzando la codifica entropica MANIAC. I pixel possono essere codificati utilizzando una codifica interlacciata o non interlacciata.

### Metodo interlacciato ###

In questo metodo vengono definiti i livelli di zoom. Il livello di zoom 0 viene utilizzato per l'immagine intera, il livello di zoom 1 viene utilizzato per tutte le righe pari, il livello di zoom 2 viene utilizzato per tutte le colonne di livello pari di zoom 1. In altre parole, ogni livello di zoom 2k con numero pari è una versione ridotta immagine, in scala 1:2^k. I livelli di zoom sono codificati dal più alto al più basso.

### Metodo non interlacciato ###

In questo metodo inizia immediatamente la codifica degli alberi MANIAC seguita dalla codifica dei pixel.

## Riferimenti ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

