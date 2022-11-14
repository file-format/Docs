---
date: 2019-12-13
keywords: m3u, formato file m3u, estensione .m3u, playlist multimediale m3u, formato playlist m3u
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file M3U e le API che possono creare e aprire file M3U."
title: Formato file M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Che cos'è un file M3U? ##

M3U (URL MP3) è un file di playlist audio memorizzato con estensione .m3u. M3U non è un vero file audio, punta solo a file audio e talvolta video. M3U è stato sviluppato per essere utilizzato con il software Winplay3 da Fraunhofer. È inoltre supportato da vari lettori multimediali e software.

## Formato file M3U

Non ci sono specifiche ufficiali per il formato di file M3U, è uno standard de facto. M3U è un file di testo normale che utilizza l'estensione .m3u se il testo è codificato nella codifica non Unicode predefinita del sistema locale o con l'estensione .m3u8 se il testo è codificato in UTF-8. Ciascuna voce nel file M3U può essere una delle seguenti:

- Percorso assoluto del file
- Percorso del file relativo al file M3U.
- URL

### M3U esteso ###

Nella M3U estesa, vengono introdotte direttive aggiuntive che iniziano con "#" e terminano con due punti(:) se hanno parametri. Di seguito è riportato un elenco di direttive per M3U esteso.

- **#EXTM3U** - È l'intestazione del file che indica M3U esteso e deve essere la prima riga del file.
- **#EXTENC:** - Codifica del testo. Deve essere la seconda riga del file.
- **#EXTINF:** - Utilizzato per informazioni sulla traccia e altre proprietà aggiuntive.
- **#PLAYLIST:** - Il titolo della playlist
- **#EXTGRP:** - Inizia il raggruppamento dei nomi
- **#EXTALB:** - Informazioni sull'album
- **#EXTART:** - Artista dell'album
- **#EXTGENRE** - Genere dell'album
- **#EXTM3A** - Playlist di file singoli per brani o capitoli di album.
- **#EXTBYT:** - Dimensioni del file in byte.
- **#EXTBIN:** - Seguono i dati binari.
- **#EXTIMG:** - Logo, copertina o altre immagini.

### HLS M3U ###

HLS (HTTP Live Streaming) è stato creato da Apple per lo streaming di audio e radio su dispositivi iOS. Si basa sull'M3U esteso con codifica UTF-8. È stato standardizzato come RFC 8216 nel 2017 da IETF. I tag per la playlist HLS iniziano con "#EXT-X-". Di seguito è riportato un elenco di tag per HLS

- **EXT-X-VERSION** - Indica la versione di compatibilità del file in base al supporto e al relativo server.
- **#EXT-X-START:** - Indica il punto di partenza preferito per la playlist.
- **#EXT-X-PLAYLIST-TYPE:** - Fornisce il tipo di playlist (EVENT o VOD).
- **#EXT-X-TARGETDURATION:** - Specifica la durata massima del Segmento.
- **#EXT-X-MEDIA-SEQUENCE:** - Indica il Media Sequence Number.
- **#EXT-X-SEGMENTI-INDIPENDENTI** - Indica che tutti i campioni di supporto sono indipendenti e possono essere decodificati senza altri segmenti.
- **#EXT-X-MEDIA:** - Viene utilizzato per mettere in relazione playlist multimediali che contengono versioni alternative dello stesso contenuto.
- **#EXT-X-STREAM-INF:** - Specifica un Variant Stream che fa parte delle Renditions.
- **#EXT-X-BYTERANGE:** - Indica che il segmento multimediale è un sottointervallo della risorsa identificata dal relativo URI.
- **#EXT-X-DISCONTINUITY** - Indica la discontinuità tra i segmenti multimediali precedenti e successivi.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Consente la sincronizzazione tra diverse interpretazioni dello stesso Variant Stream o diversi Variant Stream.
- **#EXT-X-KEY:** - Specifica come decrittografare i segmenti multimediali.
- **#EXT-X-MAP:** - Specifica come ottenere la sezione di inizializzazione del supporto. È necessario analizzare i segmenti multimediali applicabili.
- **#EXT-X-PROGRAM-DATE-TIME:** - Associa il primo campione del Segmento Media ad una data e/o ora assoluta.
- **#EXT-X-DATERANGE:** - Associa un Data Range.
- **#EXT-XI-SOLO-FRAME** - Indica che ogni segmento multimediale nella playlist descrive un singolo I-frame.
- **EXT-XI-FRAME-STREAM-INF** - Indica che il file della playlist contiene I-frame di presentazione multimediale.
- **#EXT-X-SESSION-DATA:** - Consente di visualizzare dati di sessione arbitrari
trasportato in una playlist principale.
- **#EXT-X-SESSION-KEY:** - Consente la crittografia delle chiavi. Il client può precaricare queste chiavi senza prima leggere la playlist.
- **#EXT-X-ENDLIST** - Indica che non verranno aggiunti altri segmenti multimediali al file.

Di seguito è riportato l'elenco dei tipi di media Internet utilizzati da M3U:

- **application/vnd.apple.mpegurl**: è l'unico tipo di supporto registrato (registrato nel 2009) per M3U utilizzato per fare riferimento alle playlist nelle applicazioni HLS.
- I seguenti tipi di media Internet vengono utilizzati da applicazioni non HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Esempio M3U ##

Questo è un esempio del file M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Riferimenti ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Streaming live HTTP](https://tools.ietf.org/html/rfc8216)

