---
date: 2019-12-13
keywords: ogg, format de fișier ogg, extensie .ogg, format audio ogg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier OGG și despre API-urile care pot crea și deschide fișiere OGG."
title: Fișier OGG - Fișier audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Ce este un fișier OGG?

OGG este un fișier audio comprimat Ogg Vorbis care este salvat cu extensia .ogg. Fișierele OGG sunt folosite pentru stocarea datelor audio și pot include, de asemenea, informații despre artist și piese și metadate. OGG este un format de container gratuit și deschis, care este întreținut de Fundația Xiph.Org.

## Scurt istoric al formatului de fișier OGG

Proiectul Ogg a început ca parte a unui proiect mai mare în 1993 și a fost numit Squish, dar din cauza unei mărci comerciale existente, a fost redenumit în OggSquish. A fost descrisă ca o încercare de a crea un format audio comprimat flexibil pentru aplicațiile audio moderne. Referința OGG a fost separată de Vorbis pe 2 septembrie 2000.

OGM a fost creat în 2002 din cauza lipsei de suport video oficial în OGG. Acest lucru a permis încorporarea video din cadrul Microsoft DirectShow într-un wrapper bazat pe OGG. Până în 2006, OGG a fost susținut de multe motoare de jocuri video și a fost folosit în mod obișnuit pentru a codifica conținut gratuit. Free Software Foundation a început o campanie pe 15 mai 2007, pentru a crește utilizarea Vorbis ca alternativă superioară MP3. Până la 30 iunie 2009, OGG era singurul format de container acceptat de implementarea HTML5 a Firefox 3.5.

## Format de fișier OGG

Formatul OGG constă din bucăți de date. Fiecare bucată se numește o pagină Ogg. Fiecare pagină începe cu „OggS” pentru a identifica formatul Ogg. Antetul conține numărul de serie și numărul paginii care identifică fiecare pagină ca parte a unei serii. Pagina este formată din următoarele componente.

- **Antetul paginii**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Valoare | Descriere |
| --- | --- | --- |
| 0 | 0x01 | Indică faptul că primul pachet al paginii este continuarea pachetului anterior în fluxul de biți logic. |
| 1 | 0x02 | Indică faptul că această pagină este prima din fluxul de biți logic. |
| 2 | 0x04 | Indică faptul că această pagină este ultima din fluxul de biți logic. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadate**: VorbisComment este cel mai acceptat mecanism pentru stocarea metadatelor. Alte mecanisme includ următoarele:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referințe ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

