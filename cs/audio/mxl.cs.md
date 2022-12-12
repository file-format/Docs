---
date: 2022-03-20
keywords: mxl, formát souboru Musepack, přípona .mxl
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o formátu souboru MXL a rozhraních API, která mohou vytvářet a otevírat soubory MXL."
title: Formát souboru MXL – komprimovaný soubor MusicXML
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Co je soubor MXL?

Soubor MXL je komprimovaná forma formátu souboru MusicXML, což je otevřený standardní formát pro výměnu digitálních not. Prostý text Soubory MusicXML mají velkou velikost a použití takových souborů jako formátu distribuce listů bylo ovlivněno velkou velikostí souboru. Tento problém byl vyřešen pomocí [MusicXML](https://www.musicxml.com/) 2.0 zavedením formátu souboru MXL, který komprimuje soubory dostatečně, aby se zmenšila velikost souboru podobná velikosti původních souborů MIDI. Doporučený typ média pro soubory MXL je application/vnd.recordare.musicxml.

## Formát souboru MXL

Soubory MXL jsou uloženy jako [ZIP](/cs/compression/zip/) komprimované [XML](/cs/web/xml/) soubory s příponou .mxl. Soubory MXL jsou komprimovány pomocí algoritmu DEFLATE, jak je uvedeno v [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt).

### Struktura souboru MXL

Každý soubor MXL má formát XML založený na ZIP, který musí mít soubor META-INF/container.xml, který popisuje počáteční bod verze souboru MusicXML. Pro formát souboru MXL není definován žádný odpovídající soubor .xsd.

Jednoduchý soubor container.xml má následující obsah. Tento příklad je převzat ze souboru Dichterliebe01.mxl dostupného na webu MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
V tomto příkladu je<container> element je element dokumentu. The<rootfiles> prvek může obsahovat jeden nebo více<rootfile> prvky, s první<rootfile> prvek popisující kořen MusicXML. Soubor MusicXML použitý jako a<rootfile> mohou mít<score-partwise> ,<score-timewise> nebo<opus> jako jeho dokumentový prvek.

## Reference

* [Komprimované soubory MXL](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

