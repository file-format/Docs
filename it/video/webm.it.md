---
date: 2019-10-11
keywords: WEBM, Cos'è un file WEBM, Formato file WEBM
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Scopri il formato di file WEBM e le API che possono creare e aprire file WEBM."
title: WEBM - Formato file video WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Che cos'è un file WEBM?

Un file con estensione .webm è un file video basato sul formato di file WebM aperto e privo di royalty. È stato progettato per la condivisione di video sul Web e definisce la struttura del contenitore dei file inclusi i formati video e audio. WebM è gratuito al 100% e implementa un'alta qualità basata su tecnologie aperte come HTML, HTTP e TCP/IP aperte a chiunque per l'implementazione. WebM è stato specificamente progettato per servire video sul Web, il che lo rende ottimizzato per lo streaming con un basso footprint computazionale. Ciò lo rende adatto per la riproduzione di video su qualsiasi dispositivo, in particolare netbook, palmari e tablet a bassa potenza.

## Formato file WEBM

La struttura del file WebM si basa su un sottoinsieme del formato di file contenitore Matroska [MKV](/it/video/mkv/). I flussi video disponibili in un file WebM vengono compressi utilizzando le tecnologie di compressione VP8 o VP9 che sono altamente efficienti nella compressione. Allo stesso modo, i flussi audio in un file WebM vengono compressi utilizzando i codec Vorbis o Opus sviluppati dalla [Xiph Foundation](https://www.xiph.org/). Tutti questi video e codec audio sono esenti da royalty e possono essere utilizzati senza alcun addebito.

Di seguito sono riportate le specifiche riepilogative per il formato di file WebM.

|Campo|Descrizione|
---|---|
|Tipo MIME |video/webm|
|Tipo MIME solo audio |audio/webm|
|Identificatore del tipo uniforme| org.webmproject.webm|
|Nome codec video| VP8 o VP9|
|Nome codec audio| Vorbis o Opus|

### Elementi WebM

WebM, essendo un sottoinsieme delle specifiche Matroska, fornisce supporto per alcune delle funzionalità Matroska. Di seguito è riportata una descrizione degli elementi supportati.

#### EBML

|Nome |Descrizione|
---|---|
|EBML|Imposta le caratteristiche EBML dei dati da seguire. Ogni documento EBML deve iniziare con questo.|
|EBMLVersion |La versione del parser EBML utilizzato per creare il file.|
|EBMLReadVersion|La versione EBML minima che un parser deve supportare per leggere questo file.|
|EBMLMaxIDLength |La lunghezza massima degli ID che troverai in questo file (4 o meno in Matroska).|
|EBMLMaxSizeLength|La lunghezza massima delle dimensioni che troverai in questo file (8 o meno in Matroska). Ciò non sovrascrive la dimensione dell'elemento indicata all'inizio di un elemento. Gli elementi che hanno una dimensione indicata maggiore di quella consentita da EBMLMaxSizeLength saranno considerati non validi.|
|DocType|Una stringa che descrive il tipo di documento che segue questa intestazione EBML ("webm" nel nostro caso).|
|DocTypeVersion|La versione dell'interprete DocType usata per creare il file.|
|DocTypeReadVersion|La versione minima di DocType che un interprete deve supportare per leggere questo file.|

#### Elementi globali

Al momento, è supportato solo l'elemento `Void` che viene utilizzato per annullare i dati danneggiati, per evitare comportamenti imprevisti quando si utilizzano dati danneggiati. Il contenuto viene scartato. Utilizzato anche per riservare spazio in un sottoelemento per un uso successivo.

#### Segmento
Questo elemento contiene tutti gli altri elementi di primo livello (livello 1). Tipicamente un file Matroska è composto da 1 segmento.

#### Meta Cerca informazioni

Le seguenti informazioni di ricerca sono supportate.

|Nome elemento |Descrizione|
---|---|
|SeekHead |Contiene la posizione di un altro elemento di livello 1.|
|Seek |Contiene una singola voce di ricerca in un elemento EBML.|
|SeekID |L'ID binario corrispondente al nome dell'elemento.|
|SeekPosition |La posizione dell'elemento nel segmento in ottetti (0 = primo elemento di livello 1).|

## Riferimenti

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)

