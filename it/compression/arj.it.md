---
date: 2019-12-09
keywords: arj, .arj, formato di file arj, come aprire i file arj, estensione .arj, estensione arj
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file ARJ
linktitle: ARJ
description: "Scopri il formato di file ARJ e le API che possono creare e aprire file ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Che cos'è un file ARJ? ##

ARJ (Archiviato da Robert Jung) è un file di archivio compresso ad alta efficienza sviluppato da Robert K. Jung. ARJ è stato sviluppato per DOS e le prime versioni di Windows all'inizio degli anni '90. I file ARJ sono utili per il backup o la condivisione di un numero elevato di file poiché non è necessario tenere traccia di tutti quei file e c'è un solo file da gestire. L'estensione .arj viene utilizzata per i file di archivio ARJ.

## Formato file ARJ ##

Un file ARJ contiene due tipi di intestazioni:

- Intestazione principale: c'è un'intestazione principale all'inizio dell'archivio.
- Intestazioni locali: le intestazioni locali sono presenti prima di ogni file.

|Offset|Tipo|Conteggio|Descrizione|
|---|---|---|---|
|0000h|parola|1|ID=0EA60h|
|0002h|parola|1|dimensione intestazione di base|
|0004h|byte|1|Dimensione dell'intestazione|
|0005h|byte|1|Numero versione archivio|
|0006h|byte|1|Numero di versione minimo necessario|
|0007h|byte|1|OS host:</br> 0 - MS-DOS</br> 1 - PRIMO</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Sistema xx)</br> 5 - OS/2</br> 6 - MELA GS</br> 7 - Atari ST</br> 8 - Successivo</br> 9 - VAX VMS|
|0008h|byte|1|Flag interni, bitmap:</br> 0 - nessuna password/password</br> 1 - riservato</br> 2 - il file continua sul disco successivo</br> 3 - il campo della posizione iniziale del file è disponibile</br> 4 - traduzione di percorsi ( da "\" a "/" )|
|0009h|byte|1|Metodo di compressione:</br> 0 - memorizzato</br> 1 - compresso di più</br> 2 - compresso</br> 3 - compresso più velocemente</br> 4 - compresso più veloce|
|000Ah|byte|1|Tipo di file:</br> 0 - binario</br> 1 - testo a 7 bit</br> 2 - intestazione del commento</br> 3 - directory</br> 4 - etichetta del volume|
|000Bh|byte|1|riservato|
|000Ch|dword|1|Data/ora del file originale in formato MS-DOS|
|0010h|dword|1|Dimensione del file compresso|
|0014h|dword|1|Dimensione del file originale"|
|0018h|dword|1|CRC-32 del file originale|
|001Ah|parola|1|Posizione specifica del file nel nome del file|
|001Ch|parola|1|Attributi del file|
|001Eh|parola|1|Dati host|
|?|dword|1|Posizione iniziale del file esteso|
|????h|dword|1|CRC-32 dell'intestazione di base|
|????h|parola|1|Dimensione della prima intestazione estesa|
|????h+"SIZ"+2|dword|1|CRC-32 dell'intestazione estesa|
|????h+"SIZ"+6|byte|?|File compresso|

## Riferimenti ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

