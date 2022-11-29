---
date: 2022-03-20
keywords: mxl, Musepack-filformat, .mxl-tillägg
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig om MXL-filformat och API:er som kan skapa och öppna MXL-filer." 
title: MXL-filformat - Komprimerad MusicXML-fil
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Vad är en MXL fil?

En MXL-fil är den komprimerade formen av MusicXML-filformat som är ett öppet standardformat för utbyte av digitala noter. MusikXML-filer i vanlig text är stora och användningen av sådana filer som ett distributionsformat för ark påverkades av den stora filstorleken. Detta problem behandlades med [MusicXML](https://www.musicxml.com/) 2.0 genom att introducera MXL-filformatet som komprimerar filerna tillräckligt för att minska filstorleken liknande den för original-MIDI-filer. Rekommenderad mediatyp för MXL-filer är application/vnd.recordare.musicxml.

## MXL filformat

MXL-filer lagras som [ZIP](/sv/compression/zip/) komprimerade [XML](/sv/web/xml/)-filer med filtillägget .mxl. MXL-filer komprimeras med DEFLATE-algoritmen som specificeras i [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL-filstruktur

Varje MXL-fil har ett ZIP-baserat XML-format som måste ha en META-INF/container.xml-fil som beskriver startpunkten för MusicXML-versionen av filen. Det finns ingen motsvarande .xsd-fil definierad för MXL-filformatet.

En enkel container.xml-fil har följande innehåll. Det här exemplet är hämtat från filen Dichterliebe01.mxl som finns tillgänglig på MakeMusics webbplats.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
I det här exemplet är<container> element är dokumentelementet. De<rootfiles> element kan innehålla en eller flera<rootfile> element, med den första<rootfile> element som beskriver MusicXML-roten. En MusicXML-fil som används som en<rootfile> kan ha<score-partwise> ,<score-timewise> , eller<opus> som dess dokumentelement.

## Referenser

* [Komprimerade MXL-filer](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

