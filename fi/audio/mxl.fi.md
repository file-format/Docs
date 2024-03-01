---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lansaitse MXL-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata MXL-tiedostons.
title: MXL-tiedostomuoto - Pakattu musiikkiXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Mikä on MXL-tiedosto?

MXL-tiedosto on pakattu muoto MusicXML-tiedostomuodosta, joka on avoin standardimuoto digitaalisten nuottien vaihtoon. Pelkkä teksti MusicXML-tiedostot ovat kooltaan suuria, ja suuri tiedostokoko vaikutti tällaisten tiedostojen käyttöön arkkien jakelumuodossa. Nämä ongelmat korjattiin [MusicXML](https://www.musicxml.com/) 2.0:lla ottamalla käyttöön MXL-tiedostomuoto, joka pakkaa tiedostot tarpeeksi pienentämään tiedostokokoa, joka vastaa alkuperäisten MIDI-tiedostojen kokoa. MXL-tiedostoille suositeltu mediatyyppi on application/vnd.recordare.musicxml.

## MXL-tiedostomuoto

MXL-tiedostot tallennetaan [ZIP](/compression/zip/)-pakattuina [XML](/web/xml/)-tiedostoina, joiden tiedostotunniste on .mxl. MXL-tiedostot pakataan DEFLATE-algoritmilla, joka määritetään kohdassa [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL-tiedostorakenne

Jokaisella MXL-tiedostolla on ZIP-pohjainen XML-muoto, jossa on oltava META-INF/container.xml-tiedosto, joka kuvaa tiedoston MusicXML-version aloituskohdan. MXL-tiedostomuodolle ei ole määritetty vastaavaa .xsd-tiedostoa.

Yksinkertaisen container.xml-tiedoston sisältö on seuraava. Tämä esimerkki on otettu Dichterliebe01.mxl-tiedostosta, joka on saatavilla MakeMusic-verkkosivustolla.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Tässä esimerkissä<container> elementti on asiakirjaelementti. The<rootfiles> elementti voi sisältää yhden tai useamman<rootfile> elementtejä ensimmäisen kanssa<rootfile> elementti, joka kuvaa MusicXML-juurta. MusicXML-tiedosto, jota käytetään a<rootfile> voi olla<score-partwise> ,<score-timewise> , tai<opus> sen asiakirjaelementtinä.

## Viitteet

* [Pakatut MXL-tiedostot](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


