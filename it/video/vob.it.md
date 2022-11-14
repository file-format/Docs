---
date: 2019-10-11
keywords: vob, .vob, formato file vob, formato file .vob, estensione .vob, estensione vob, formato video vob, file dvd vob
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Scopri il formato di file VOB e le API che possono creare e aprire file VOB."
title: Formato file VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Che cos'è un file VOB? ##

I file VOB sono generalmente memorizzati nella directory VIDEO_TS su un DVD con estensione .vob. I file VOB contengono dati video e audio, nonché altri dati come menu e sottotitoli. VOB si basa sul formato del flusso di programma MPEG-2 ma ha limitazioni e specifiche aggiuntive nei flussi privati. I file VOB sono un sottoinsieme rigoroso dei flussi di programmi MPEG, quindi tutti i file VOB sono flussi di programmi MPEG ma tutti i flussi di programmi MPEG non sono compatibili con VOB.

## Struttura del video DVD ##

Quando un DVD viene aperto su un computer, VIDEO_TS è la directory di livello superiore con AUDIO_TS. AUDIO_TS è vuoto e non viene utilizzato. All'interno della directory VIDEO_TS ci sono file VOB, BUP e IFO. I file VOB contengono il contenuto MPEG. Questi sono suddivisi in blocchi da 1 GB o meno in modo che siano compatibili con tutti i sistemi operativi. I file IFO contengono informazioni riguardanti i menu e la struttura del titolo. I file BUK sono file di backup dei file IFO con lo stesso nome. Questi file devono essere conservati fisicamente in un'area separata in modo che nel caso in cui il file IFO sia danneggiato a causa di danni fisici al DVD, il file BUK possa fornire le stesse informazioni.

### Disposizione fisica ###

- Tutti i file sul disco devono essere contigui.
- I file correlati devono essere uno accanto all'altro (VOB, IFO, BUP).
- I file numerati devono essere in ordine crescente.

## Protezione dalla copia ##

Molti DVD video sono crittografati e impediscono la copia dei dati dal DVD. Le chiavi di autenticazione e decrittografia sono necessarie per riprodurre i file che si trovano nell'area inaccessibile del DVD. Queste chiavi vengono utilizzate dal software di decrittazione CSS presente nel lettore DVD o nel lettore software. Senza le chiavi, i file video non possono essere riprodotti poiché le chiavi verranno richieste all'apertura dei file.

## Riferimenti ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [All'interno del DVD-Video/Struttura della directory](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

