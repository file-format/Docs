---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lnopelniet par MXL faila formātu un API, kas var izveidot un atvērt MXL failus.
title: MXL faila formāts — saspiesta mūzikaXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Kas ir MXL fails?

MXL fails ir saspiesta MusicXML faila formāta forma, kas ir atvērta standarta formāts digitālo nošu apmaiņai. Vienkāršā teksta MusicXML faili ir lieli, un lielais faila izmērs ietekmēja šādu failu izmantošanu kā lokšņu izplatīšanas formātu. Šīs problēmas tika novērstas, izmantojot [MusicXML](https://www.musicxml.com/) 2.0, ieviešot MXL faila formātu, kas pietiekami saspiež failus, lai samazinātu faila lielumu, kas ir līdzīgs oriģinālo MIDI failu izmēram. Ieteicamais multivides veids MXL failiem ir application/vnd.recordare.musicxml.

## MXL faila formāts

MXL faili tiek glabāti kā [ZIP](/compression/zip/) saspiesti [XML](/web/xml/) faili ar .mxl faila paplašinājumu. MXL faili tiek saspiesti, izmantojot DEFLATE algoritmu, kā norādīts [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL faila struktūra

Katram MXL failam ir uz ZIP bāzes veidots XML formāts, kuram ir jābūt META-INF/container.xml failam, kas apraksta faila MusicXML versijas sākumpunktu. MXL faila formātam nav definēts atbilstošs .xsd fails.

Vienkārša faila container.xml saturs ir šāds. Šis piemērs ir ņemts no Dichterliebe01.mxl faila, kas pieejams MakeMusic vietnē.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Šajā piemērā<container> elements ir dokumenta elements. The<rootfiles> elements var saturēt vienu vai vairākus<rootfile> elementi, ar pirmo<rootfile> elements, kas apraksta MusicXML sakni. MusicXML fails, ko izmanto kā a<rootfile> var būt<score-partwise> ,<score-timewise> , vai<opus> kā tā dokumenta elementu.

## Atsauces

* [Saspiestie MXL faili](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


