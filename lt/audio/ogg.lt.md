---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie OGG failo formatą ir API, kurios gali sukurti ir atidaryti OGG failąs.
title: OGG failas – Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Kas yra OGG failas?

OGG yra Ogg Vorbis suspaustas garso failas, kuris išsaugomas su plėtiniu .ogg. OGG failai naudojami garso duomenims saugoti ir gali apimti atlikėjo ir takelio informaciją bei metaduomenis. OGG yra nemokamas ir atviras konteinerio formatas, kurį prižiūri Xiph.Org Foundation.

## Trumpa OGG failo formato istorija

Ogg projektas buvo pradėtas kaip didesnio projekto dalis 1993 m. ir buvo pavadintas Squish, tačiau dėl esamo prekės ženklo jis buvo pervadintas į OggSquish. Tai buvo apibūdinta kaip bandymas sukurti lankstų suspausto garso formatą šiuolaikinėms garso programoms. OGG nuoroda buvo atskirta nuo Vorbis 2000 m. rugsėjo 2 d.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. Iki 2009 m. birželio 30 d. OGG buvo vienintelis konteinerio formatas, palaikomas HTML5 3.5 versijos Firefox.

## OGG failo formatas

OGG formatas susideda iš duomenų dalių. Kiekvienas gabalas vadinamas Ogg puslapiu. Kiekvienas puslapis prasideda OggS, kad būtų galima identifikuoti Ogg formatą. Antraštėje yra serijos numeris ir puslapio numeris, kuris identifikuoja kiekvieną puslapį kaip serijos dalį. Puslapį sudaro šie komponentai.

- **Puslapio antraštė**
  - "**Capture Pattern (32 bitai)**: naudojamas sinchronizuoti analizuojant OGG failus."
  - "**Versija (8 bitai)**: nurodo Ogg bitų srauto versiją."
  - "**Antraštės tipas (8 bitai)**: nurodo puslapio tipą."

| Bit | Vertė | Aprašymas |
| --- | --- | --- |
| 0 | 0x01 | Nurodo, kad pirmasis puslapio paketas yra ankstesnio paketo tęsinys loginiame bitų sraute. |
| 1 | 0x02 | Nurodo, kad šis puslapis yra pirmasis loginiame bitų sraute. |
| 2 | 0x04 | Nurodo, kad šis puslapis yra paskutinis loginiame bitų sraute. |

  - "**Granulės padėtis (64 bitai)**: tai laiko žymeklis, kurio reikšmę nustato kodekas."
  - "**Bitstream serijos numeris (32 bitai)**: tai serijos numeris, identifikuojantis puslapį, priklausantį tam tikram loginiam bitų srautui."
  - "**Puslapio sekos numeris (32 bitai)**: nurodo puslapio seką, kurio pirmasis puslapis prasideda nuo 0."
  - "**Checksum (32 bits)**: pateikia viso puslapio duomenų CRC32 kontrolinę sumą."
  - "**Puslapio segmentai (8 bitai)**: nurodo segmentų skaičių puslapyje."
  - "**Segmentų lentelė**: tai 8 bitų reikšmių masyvas, nurodantis kiekvieno puslapio teksto segmento ilgį."
– **Metaduomenys**: VorbisComment yra plačiausiai palaikomas metaduomenų saugojimo mechanizmas. Kiti mechanizmai yra šie:
  - "FLAC metaduomenų blokai"
  - "Ogg skeletas"
  - "Nuolatinė medijos žymėjimo kalba"

## Nuorodos Nr.

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

