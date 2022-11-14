---
date: 2019-12-13
keywords: ogg, ogg-bestandsindeling, .ogg-extensie, ogg-audioformaat
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over OGG-bestandsindeling en API's die OGG-bestanden kunnen maken en openen."
title: OGG-bestand - Ogg Vorbis-audiobestand
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Wat is een OGG-bestand?

OGG is een Ogg Vorbis gecomprimeerd audiobestand dat wordt opgeslagen met de .ogg-extensie. OGG-bestanden worden gebruikt voor het opslaan van audiogegevens en kunnen ook artiest- en trackinformatie en metadata bevatten. OGG is een gratis en open containerformaat dat wordt onderhouden door Xiph.Org Foundation.

## Korte geschiedenis van OGG-bestandsindeling

Het Ogg-project begon als onderdeel van een groter project in 1993 en heette Squish, maar vanwege een bestaand handelsmerk werd het omgedoopt tot OggSquish. Het werd beschreven als een poging om een flexibel gecomprimeerd audioformaat te creëren voor moderne audiotoepassingen. OGG-referentie werd op 2 september 2000 gescheiden van Vorbis.

OGM is in 2002 opgericht vanwege het ontbreken van formele video-ondersteuning in OGG. Hierdoor kon video van het Microsoft DirectShow-framework worden ingesloten in een op OGG gebaseerde wrapper. In 2006 werd OGG ondersteund door veel videogame-engines en werd het vaak gebruikt om gratis inhoud te coderen. De Free Software Foundation startte op 15 mei 2007 een campagne om het gebruik van Vorbis als superieur alternatief voor MP3 te vergroten. Op 30 juni 2009 was OGG het enige containerformaat dat werd ondersteund door de HTML5-implementatie van Firefox 3.5.

## OGG-bestandsindeling

Het OGG-formaat bestaat uit stukjes data. Elke chunk wordt een Ogg-pagina genoemd. Elke pagina begint met "OggS" om het Ogg-formaat te identificeren. De koptekst bevat het serienummer en paginanummer dat elke pagina identificeert als onderdeel van een serie. De pagina bestaat uit de volgende onderdelen.

- **Pagina hoofd**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Beetje | Waarde | Beschrijving |
| --- | --- | --- |
| 0 | 0x01 | Geeft aan dat het eerste pakket van de pagina de voortzetting is van het vorige pakket in de logische bitstroom. |
| 1 | 0x02 | Geeft aan dat deze pagina de eerste is in de logische bitstream. |
| 2 | 0x04 | Geeft aan dat deze pagina de laatste is in de logische bitstream. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadata**: VorbisComment is het meest algemeen ondersteunde mechanisme voor het opslaan van metadata. Andere mechanismen zijn onder meer:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referenties ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

