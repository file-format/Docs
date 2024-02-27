---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltjene om MXL filformat og API'er, der kan oprette og åbne MXL fils.
title: MXL-filformat - Komprimeret MusicXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Hvad er en MXL fil?

En MXL-fil er den komprimerede form for MusicXML-filformat, der er et åbent standardformat til udveksling af digitale noder. Almindelig tekst MusicXML-filer er store i størrelse, og brugen af sådanne filer som et ark distributionsformat blev påvirket af den store filstørrelse. Dette problem blev behandlet med [MusicXML](https://www.musicxml.com/) 2.0 ved at introducere MXL-filformatet, der komprimerer filerne nok til at reducere filstørrelsen svarende til den for originale MIDI-filer. Den anbefalede medietype til MXL-filer er application/vnd.recordare.musicxml.

## MXL filformat

MXL-filer gemmes som [ZIP](/compression/zip/)-komprimerede [XML](/web/xml/)-filer med .mxl-filtypen. MXL-filer komprimeres med DEFLATE-algoritmen som angivet i [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL-filstruktur

Hver MXL-fil har et ZIP-baseret XML-format, der skal have en META-INF/container.xml-fil, som beskriver udgangspunktet for MusicXML-versionen af filen. Der er ingen tilsvarende .xsd-fil defineret for MXL-filformatet.

En simpel container.xml-fil har indholdet som følger. Dette eksempel er taget fra filen Dichterliebe01.mxl, der er tilgængelig på MakeMusic-webstedet.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
I dette eksempel er<container> element er dokumentelementet. Det<rootfiles> element kan indeholde en eller flere<rootfile> elementer, med det første<rootfile> element, der beskriver MusicXML-roden. En MusicXML-fil, der bruges som en<rootfile> kan have<score-partwise> ,<score-timewise> , eller<opus> som dokumentelement.

## Referencer

* [Komprimerede MXL-filer](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


