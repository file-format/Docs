---
date: 2019-10-11
keywords: srt, .srt, formato file srt, formato file .srt, estensione .srt, estensione srt
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Informazioni sul formato di file SRT e sulle API che possono creare e aprire file SRT."
title: Formato file SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Che cos'è un file SRT? ##

SRT (SubRip file format) è un semplice file di sottotitoli salvato nel formato di file SubRip con estensione .srt. Contiene un numero sequenziale di sottotitoli, timestamp di inizio e fine e testo dei sottotitoli. I file SRT consentono di aggiungere sottotitoli al contenuto video dopo che è stato prodotto.

## Struttura del file SRT ##

Ogni sottotitolo ha quattro parti nel file SRT.

1. Un contatore numerico che indica il numero o la posizione del sottotitolo.
1. Ora di inizio e fine del sottotitolo separate da --> caratteri
1. Testo dei sottotitoli in una o più righe.
1. Una riga vuota che indica la fine del sottotitolo.

### Esempio di SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Per specificare l'ora viene utilizzato il formato *ore:minuti:secondi,millisecondi (00:00:00,000)*.

## Formattazione dei file SRT ##

La formattazione dei file SRT è derivata da tag HTML. I tag di formattazione per il file SRT sono elencati di seguito.

| Effetto | tag |
| --- | --- |
|Grassetto|**\ <b>...\</b> ** o {b}...{/b}|
|Corsivo|**\ <i>...\</i> ** o **{i}...{/i}**|
|Sottolineato|**\ <u>...\</u> ** o **{u}...{/u}**|
|Colore carattere|**\ <font color="white">...\</font> **|
|Posizione riga|**{\a3}** (indica che il testo dovrebbe iniziare ad apparire sulla riga 3)

## Software SubRip ##

SubRip è un programma software gratuito che funziona su Windows. Estrae i sottotitoli e i loro tempi da diversi formati video e salva i sottotitoli in formato SRT. SubRip utilizza il riconoscimento ottico dei caratteri per estrarre i sottotitoli da video live, altri file video e DVD.

## Riferimenti ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
