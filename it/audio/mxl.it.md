---
date: 2022-03-20
keywords: mxl, formato file Musepack, estensione .mxl
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Scopri il formato di file MXL e le API che possono creare e aprire file MXL."
title: Formato file MXL - File MusicXML compresso
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Che cos'è un file MXL?

Un file MXL è la forma compressa del formato di file MusicXML che è un formato standard aperto per lo scambio di spartiti digitali. I file MusicXML di testo normale sono di grandi dimensioni e l'uso di tali file come formato di distribuzione dei fogli è stato influenzato dalle grandi dimensioni del file. Questo problema è stato trattato con [MusicXML](https://www.musicxml.com/) 2.0 introducendo il formato di file MXL che comprime i file abbastanza da ridurre la dimensione del file simile a quella dei file MIDI originali. Il tipo di supporto consigliato per i file MXL è application/vnd.recordare.musicxml.

## Formato file MXL

I file MXL vengono archiviati come file compressi [ZIP](/it/compression/zip/) [XML](/it/web/xml/) con estensione .mxl. I file MXL sono compressi con l'algoritmo DEFLATE come specificato in [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Struttura del file MXL

Ogni file MXL ha un formato XML basato su ZIP che deve avere un file META-INF/container.xml che descrive il punto di partenza della versione MusicXML del file. Non esiste un file .xsd corrispondente definito per il formato file MXL.

Un semplice file container.xml ha i contenuti come segue. Questo esempio è tratto dal file Dichterliebe01.mxl disponibile sul sito Web di MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
In questo esempio, il<container> element è l'elemento del documento. Il<rootfiles> l'elemento può contenerne uno o più<rootfile> elementi, con il primo<rootfile> elemento che descrive la radice di MusicXML. Un file MusicXML utilizzato come file<rootfile> potrebbe avere<score-partwise> ,<score-timewise> , o<opus> come suo elemento di documento.

## Riferimenti

* [File MXL compressi](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

