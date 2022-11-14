---
date: 2022-03-20
keywords: mxl, Musepack-bestandsindeling, .mxl-extensie
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Meer informatie over de MXL-bestandsindeling en API's die MXL-bestanden kunnen maken en openen."
title: MXL-bestandsindeling - Gecomprimeerd MusicXML-bestand
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Wat is een MXL-bestand?

Een MXL-bestand is de gecomprimeerde vorm van het MusicXML-bestandsformaat dat een open standaardformaat is voor het uitwisselen van digitale bladmuziek. Platte tekst MusicXML-bestanden zijn groot en het gebruik van dergelijke bestanden als bladdistributieformaat werd beïnvloed door de grote bestandsgrootte. Dit probleem is verholpen met [MusicXML](https://www.musicxml.com/) 2.0 door de introductie van het MXL-bestandsformaat dat de bestanden voldoende comprimeert om de bestandsgrootte te verkleinen die vergelijkbaar is met die van originele MIDI-bestanden. Aanbevolen mediatype voor MXL-bestanden is application/vnd.recordare.musicxml.

## MXL-bestandsindeling

MXL-bestanden worden opgeslagen als [ZIP](/nl/compression/zip/) gecomprimeerde [XML](/nl/web/xml/)-bestanden met de bestandsextensie .mxl. MXL-bestanden worden gecomprimeerd met het DEFLATE-algoritme zoals gespecificeerd in de [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL-bestandsstructuur

Elk MXL-bestand heeft een ZIP-gebaseerd XML-formaat dat een META-INF/container.xml-bestand moet hebben dat het startpunt van de MusicXML-versie van het bestand beschrijft. Er is geen corresponderend .xsd-bestand gedefinieerd voor het MXL-bestandsformaat.

Een eenvoudig bestand container.xml heeft de volgende inhoud. Dit voorbeeld is afkomstig uit het bestand Dichterliebe01.mxl dat beschikbaar is op de MakeMusic-website.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
In dit voorbeeld is de<container> element is het documentelement. De<rootfiles> element kan een of meer bevatten<rootfile> elementen, met de eerste<rootfile> element dat de MusicXML-root beschrijft. Een MusicXML-bestand dat wordt gebruikt als een<rootfile> zou kunnen hebben<score-partwise> ,<score-timewise> , of<opus> als zijn documentelement.

## Referenties

* [Gecomprimeerde MXL-bestanden](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

