---
date: 2019-12-09
keywords: arc, .arc, arc filformat, hur man öppnar arc-filer, .arc extension, arc extension
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC filformat
linktitle: ARC
description: "Lär dig mer om ARC-filformat och API:er som kan skapa och öppna ARC-filer." 
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Vad är ARC fil?

ARC är ett förlustfritt datakomprimerings- och arkivformat utvecklat av System Enhancement Associates (SEA). Filformatet och programmet som skapar det kallas båda ARC. ARC var mycket populärt under de tidiga dagarna av uppringd BBS eftersom det kombinerade funktionerna med komprimering och arkivering av flera filer i samma fil. ARC ersattes senare av [ZIP](/sv/compression/zip/) som erbjöd bättre kompressionsförhållanden.

.arc-filtillägget används av flera andra icke-relaterade arkivfiltyper som ARC-formatet som används av Internet Archive för att lagra flera webbresurser, ett annat ARC-format som används av FreeArc archiver, ett annat format som används av Nintendo för resurser, etc. .

## Kort historik om ARC-filformat

ARC-programmet skrevs av Thom Henderson från System Enhancement Associates 1985. Detta program grupperade filer i en enda arkivfil och komprimerade dem också. Filerna som genererades av ARC-programmet använde tillägget .arc. SEA släppte källkoden för ARC 1986 och ARC portades till Unix och Atari ST av Howard Chu 1987.

Phil Katz utvecklade PKARC och PKXARC för att arkivera och extrahera filer. Filerna fungerade med ARC-filformatet och var betydligt snabbare. Till skillnad från ARC delade Katz komprimerings- och arkiveringsfunktionerna mellan två olika filer vilket minskade minneskravet för att köra dem.

Efter rättegången mellan SEA och Katz drog SEA sig tillbaka från shareware-marknaden och utvecklade ARC+Plus med ett helskärmsgränssnitt. ARC-formatet är inte vanligt på PC längre.

## ARC filformat

ARC-filen består av en sekvens av filhuvud och fil följt av markören för slutet av arkivet som visas nedan.

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

### ARC-filhuvud ###

|Offset|Etikett|Typ|Värde|Beskrivning|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metod|
|02|ARCFNT|DS|12|filnamn|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Komprimerad storlek|
|13|ARCDAT|DW|0000|Fildatum (MSDOS)|
|15|ARCTIM|DW|0000|Filtid (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Okomprimerad storlek|
|1D|ARCFIL|DS|ARCNSZ| |

### Komprimeringsmetoder ###

Komprimeringsmetodbyten anger vilken komprimeringsmetod som används. Följande är de komprimeringsmetoder som används för ARC-filen.

|Metod|Namn|Beskrivning|
|---|---|---|
|0|Lagrad|Ingen komprimering används|
|1|Förpackat|Upprepad kodning av löplängd (RLE)|
|2|Squeezed|Huffman-kodning|
|3|Crunched|LZW med 4K-buffert, 12 bitars koder|
|4|Crunched|Första packning, sedan LZW 4K-buffert med 12 bitar|
|5|Crunched|Packning, LZW, 4K-buffert, variabel längd (9-12 bitar)|
|6|Squashed|LZW, 8K buffert, variabel längd (9-13 bitar)|
|7|Krossad|Packning, sedan LZW 8K-buffert, 2-13 bitar (PAK 1.0)|
|8|Destillera|Dynamisk Huffman med 8K buffert (PAK 2.0)|

## Referenser

- [ARC (filformat) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

