---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC fil formularat
linktitle: ARC
description: Ltjene om ARC filformat og API'er, der kan oprette og åbne ARC fils.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Hvad er en ARC fil?

ARC er et tabsfrit datakomprimerings- og arkivformat udviklet af System Enhancement Associates (SEA). Filformatet og programmet, der opretter det, kaldes begge ARC. ARC var meget populær i de tidlige dage af dial-up BBS, da den kombinerede funktionerne ved komprimering og arkivering af flere filer i den samme fil. ARC blev senere erstattet af [ZIP](/compression/zip/), der tilbød bedre kompressionsforhold.

.arc filtypenavnet bruges af flere andre ikke-relaterede arkivfiltyper såsom ARC-formatet, der bruges af Internet Archive til at gemme flere webressourcer, et andet ARC-format, der bruges af FreeArc archiver, et andet format, der bruges af Nintendo til ressourcer osv. .

## Kort historie om ARC-filformat

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Dette program grupperede filer i en enkelt arkivfil og komprimerede dem også. Filerne genereret af ARC-programmet brugte filtypenavnet .arc. SEA udgav kildekoden til ARC i 1986, og ARC blev overført til Unix og Atari ST af Howard Chu i 1987.

Phil Katz udviklede PKARC og PKXARC til arkivering og udpakning af filer. Filerne fungerede med ARC-filformatet og var betydeligt hurtigere. I modsætning til ARC opdelte Katz komprimerings- og arkiveringsfunktionerne mellem to forskellige filer, hvilket reducerede hukommelseskravet til at køre dem.

Efter retssagen mellem SEA og Katz trak SEA sig tilbage fra shareware-markedet og udviklede ARC+Plus med en fuldskærms brugergrænseflade. ARC-formatet er ikke almindeligt på pc længere.

## ARC filformat

ARC-filen består af en sekvens af filoverskrift og fil efterfulgt af slutningen af arkivmarkøren som vist nedenfor.

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

### ARC-filoverskrift ###

|Offset|Etiket|Type|Værdi|Beskrivelse|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metode|
|02|ARCFNT|DS|12|filnavn|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Komprimeret størrelse|
|13|ARCDAT|DW|0000|Fildato (MSDOS)|
|15|ARCTIM|DW|0000|Filtid (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Ukomprimeret størrelse|
|1D|ARCFIL|DS|ARCNSZ| |

### Komprimeringsmetoder ###

Kompressionsmetode-byten angiver den anvendte komprimeringsmetode. Følgende er de komprimeringsmetoder, der bruges til ARC-filen.

|Metode|Navn|Beskrivelse|
|---|---|---|
|0|Lagret|Ingen komprimering brugt|
|1|Packed|Repeated running length encoding (RLE)|
|2|Squeezed|Huffman-kodning|
|3|Crunched|LZW med 4K buffer, 12 bit koder|
|4|Crunched|Først pakning, derefter LZW 4K buffer med 12 bit|
|5|Crunched|Packning, LZW, 4K buffer, variabel længde (9-12 bit)|
|6|Squashed|LZW, 8K buffer, variabel længde (9-13 bit)|
|7|Knust|Packning, derefter LZW 8K buffer, 2-13 bit (PAK 1.0)|
|8|Destiller|Dynamisk Huffman med 8K buffer (PAK 2.0)|

## Referencer

- [ARC (file format) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

