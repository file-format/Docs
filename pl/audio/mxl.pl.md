---
date: 2022-03-20
keywords: mxl, format pliku Musepack, rozszerzenie .mxl
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików MXL i interfejsach API, które umożliwiają tworzenie i otwieranie plików MXL."
title: Format pliku MXL — skompresowany plik MusicXML
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Czym jest plik MXL?

Plik MXL to skompresowana forma formatu pliku MusicXML, który jest otwartym standardowym formatem wymiany cyfrowych nut. Zwykły tekst Pliki MusicXML mają duży rozmiar, a użycie takich plików jako formatu dystrybucji arkuszy wpłynęło na duży rozmiar pliku. Ten problem rozwiązano w wersji [MusicXML](https://www.musicxml.com/) 2.0, wprowadzając format pliku MXL, który kompresuje pliki na tyle, aby zmniejszyć rozmiar pliku podobny do rozmiaru oryginalnych plików MIDI. Zalecany typ nośnika dla plików MXL to application/vnd.recordare.musicxml.

## Format pliku MXL

Pliki MXL są przechowywane jako [ZIP](/pl/compression/zip/) skompresowane pliki [XML](/pl/web/xml/) z rozszerzeniem pliku .mxl. Pliki MXL są kompresowane za pomocą algorytmu DEFLATE, jak określono w [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Struktura pliku MXL

Każdy plik MXL ma format XML oparty na formacie ZIP, który musi zawierać plik META-INF/container.xml opisujący punkt początkowy wersji MusicXML pliku. Nie ma odpowiedniego pliku .xsd zdefiniowanego dla formatu pliku MXL.

Prosty plik container.xml ma następującą zawartość. Ten przykład pochodzi z pliku Dichterliebe01.mxl dostępnego na stronie internetowej MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
W tym przykładzie<container> element jest elementem dokumentu. The<rootfiles> element może zawierać jeden lub więcej<rootfile> elementy, z pierwszym<rootfile> element opisujący katalog główny MusicXML. Plik MusicXML używany jako plik<rootfile> może mieć<score-partwise> ,<score-timewise> , lub<opus> jako element dokumentu.

## Bibliografia

* [Skompresowane pliki MXL](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

