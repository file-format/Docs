---
date: 2022-03-20
keywords: mxl, format de fișier Musepack, extensia .mxl
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Aflați despre formatul de fișier MXL și despre API-urile care pot crea și deschide fișiere MXL."
title: Format de fișier MXL - Fișier MusicXML comprimat
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Ce este un fișier MXL?

Un fișier MXL este forma comprimată a formatului de fișier MusicXML, care este un format standard deschis pentru schimbul de partituri digitale. Fișierele cu text simplu MusicXML au dimensiuni mari, iar utilizarea unor astfel de fișiere ca format de distribuție a foilor a fost afectată de dimensiunea mare a fișierului. Aceste probleme au fost tratate cu [MusicXML](https://www.musicxml.com/) 2.0 prin introducerea formatului de fișier MXL care comprimă fișierele suficient pentru a reduce dimensiunea fișierului similar cu cea a fișierelor MIDI originale. Tipul media recomandat pentru fișierele MXL este application/vnd.recordare.musicxml.

## Format de fișier MXL

Fișierele MXL sunt stocate ca fișiere [ZIP](/ro/compression/zip/) comprimate [XML](/ro/web/xml/) cu extensia de fișier .mxl. Fișierele MXL sunt comprimate cu algoritmul DEFLATE așa cum este specificat în [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Structura fișierului MXL

Fiecare fișier MXL are un format XML bazat pe ZIP care trebuie să aibă un fișier META-INF/container.xml care descrie punctul de plecare al versiunii MusicXML a fișierului. Nu există niciun fișier .xsd corespunzător definit pentru formatul de fișier MXL.

Un fișier container.xml simplu are conținut după cum urmează. Acest exemplu este preluat din fișierul Dichterliebe01.mxl disponibil pe site-ul web MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
În acest exemplu,<container> elementul este elementul de document. The<rootfiles> elementul poate conține unul sau mai multe<rootfile> elemente, cu primul<rootfile> element care descrie rădăcina MusicXML. Un fișier MusicXML folosit ca a<rootfile> ar putea avea<score-partwise> ,<score-timewise> , sau<opus> ca element de document al acestuia.

## Referințe

* [Fișiere MXL comprimate](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

