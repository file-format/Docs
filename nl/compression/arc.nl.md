---
date: 2019-12-09
keywords: arc, .arc, arc-bestandsindeling, hoe arc-bestanden te openen, .arc-extensie, arc-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC-bestandsindeling
linktitle: ARC
description: "Meer informatie over ARC-bestandsindelingen en API's die ARC-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Wat is een ARC-bestand?

ARC is een lossless datacompressie- en archiveringsformaat ontwikkeld door System Enhancement Associates (SEA). Het bestandsformaat en de toepassing die het maakt, worden beide ARC genoemd. ARC was erg populair tijdens de begindagen van de dial-up BBS omdat het de functies van compressie en het archiveren van meerdere bestanden in hetzelfde bestand combineerde. ARC werd later vervangen door [ZIP](/nl/compression/zip/) dat betere compressieverhoudingen bood.

De .arc-bestandsextensie wordt gebruikt door verschillende andere niet-gerelateerde archiefbestandstypen, zoals het ARC-formaat dat door het internetarchief wordt gebruikt om meerdere webbronnen op te slaan, een ander ARC-formaat dat wordt gebruikt door FreeArc-archiver, een ander formaat dat door Nintendo wordt gebruikt voor bronnen, enz. .

## Korte geschiedenis van ARC-bestandsindeling

Het ARC-programma is in 1985 geschreven door Thom Henderson van System Enhancement Associates. Dit programma groepeerde bestanden in een enkel archiefbestand en comprimeerde ze ook. De bestanden die door het ARC-programma werden gegenereerd, gebruikten de extensie .arc. SEA heeft de broncode voor ARC in 1986 vrijgegeven en ARC werd in 1987 door Howard Chu overgezet naar Unix en Atari ST.

Phil Katz ontwikkelde PKARC en PKXARC voor het archiveren en uitpakken van bestanden. De bestanden werkten met het ARC-bestandsformaat en waren aanzienlijk sneller. In tegenstelling tot ARC verdeelde Katz de compressie- en archiveringsfuncties over twee verschillende bestanden, waardoor er minder geheugen nodig was om ze uit te voeren.

Na de rechtszaak tussen SEA en Katz trok SEA zich terug uit de shareware-markt en ontwikkelde ARC+Plus met een gebruikersinterface op volledig scherm. Het ARC-formaat is niet meer gebruikelijk op pc.

## ARC-bestandsindeling

Het ARC-bestand bestaat uit een reeks van bestandskop en bestand, gevolgd door de einde-van-archiefmarkering, zoals hieronder weergegeven.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC-bestandskop ###

|Offset|Label|Type|Waarde|Beschrijving|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Methode|
|02|ARCFNT|DS|12|bestandsnaam|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Gecomprimeerde grootte|
|13|ARCDAT|DW|0000|Bestandsdatum (MSDOS)|
|15|ARCTIM|DW|0000|Bestandstijd (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Ongecomprimeerde grootte|
|1D|ARCFIL|DS|ARCNSZ| |

### Compressiemethoden ###

De byte van de compressiemethode geeft de gebruikte compressiemethode aan. Hieronder volgen de compressiemethoden die voor het ARC-bestand worden gebruikt.

|Methode|Naam|Beschrijving|
|---|---|---|
|0|Opgeslagen|Geen compressie gebruikt|
|1|Verpakt|Herhaalde codering van de looplengte (RLE)|
|2|Squeezed|Huffman-codering|
|3|Crunched|LZW met 4K-buffer, 12-bits codes|
|4|Gekneld|Eerste verpakking, daarna LZW 4K-buffer met 12 bits|
|5|Gekneld|Verpakking, LZW, 4K-buffer, variabele lengte (9-12 bits)|
|6|Squashed|LZW, 8K buffer, variabele lengte (9-13 bits)|
|7|Verpletterd|Verpakking, dan LZW 8K buffer, 2-13 bits (PAK 1.0)|
|8|Distill|Dynamische Huffman met 8K-buffer (PAK 2.0)|

## Referenties

- [ARC (bestandsformaat) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

