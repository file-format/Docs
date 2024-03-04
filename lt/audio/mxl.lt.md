---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Luždirbkite apie MXL failo formatą ir API, kurios gali sukurti ir atidaryti MXL failąs.
title: MXL failo formatas – suspausta muzikaXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Kas yra MXL failas?

MXL failas yra suspausta MusicXML failo formato forma, kuris yra atviras standartinis formatas, skirtas keistis skaitmeninėmis natomis. Paprasto teksto MusicXML failai yra didelio dydžio, todėl didelis failo dydis turėjo įtakos tokių failų naudojimui kaip lapo platinimo formatu. Šios problemos buvo išspręstos naudojant [MusicXML](https://www.musicxml.com/) 2.0, įdiegus MXL failo formatą, kuris pakankamai suglaudina failus, kad sumažintų failo dydį, panašų į originalių MIDI failų dydį. Rekomenduojamas medijos tipas MXL failams yra application/vnd.recordare.musicxml.

## MXL failo formatas

MXL failai saugomi kaip [ZIP](/compression/zip/) suglaudinti [XML](/web/xml/) failai su .mxl failo plėtiniu. MXL failai suglaudinami naudojant DEFLATE algoritmą, kaip nurodyta [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL failo struktūra

Kiekvienas MXL failas turi ZIP formato XML formatą, kuriame turi būti META-INF/container.xml failas, apibūdinantis failo MusicXML versijos pradžios tašką. MXL failo formatui nėra apibrėžto atitinkamo .xsd failo.

Paprasto konteinerio.xml failo turinys yra toks. Šis pavyzdys paimtas iš Dichterliebe01.mxl failo, esančio MakeMusic svetainėje.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Šiame pavyzdyje<container> elementas yra dokumento elementas. The<rootfiles> elemente gali būti vienas ar daugiau<rootfile> elementai, su pirmuoju<rootfile> elementas, apibūdinantis MusicXML šaknį. MusicXML failas, naudojamas kaip a<rootfile> gali turėti<score-partwise> ,<score-timewise> , arba<opus> kaip dokumento elementą.

## Nuorodos

* [Suspausti MXL failai](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


