---
date: 2019-12-09
keywords: arc, .arc, format de fișier arc, cum să deschideți fișierele arc, extensie .arc, extensie arc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier ARC
linktitle: ARC
description: "Aflați despre formatul fișierului ARC și despre API-urile care pot crea și deschide fișiere ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Ce este un fișier ARC?

ARC este un format de arhivare și compresie de date fără pierderi dezvoltat de System Enhancement Associates (SEA). Formatul de fișier și aplicația care îl creează se numesc ARC. ARC a fost foarte popular în primele zile ale BBS dial-up, deoarece combina caracteristicile de compresie și arhivare a mai multor fișiere în același fișier. ARC a fost înlocuit ulterior cu [ZIP](/ro/compression/zip/) care a oferit rapoarte de compresie mai bune.

Extensia de fișier .arc este utilizată de mai multe alte tipuri de fișiere de arhivă care nu au legătură, cum ar fi formatul ARC utilizat de Internet Archive pentru a stoca mai multe resurse web, un format ARC diferit utilizat de arhivatorul FreeArc, un format diferit utilizat de Nintendo pentru resurse etc. .

## Scurt istoric al formatului de fișier ARC

Programul ARC a fost scris de Thom Henderson de la System Enhancement Associates în 1985. Acest program a grupat fișierele într-un singur fișier de arhivă și, de asemenea, le-a comprimat. Fișierele generate de programul ARC au folosit extensia .arc. SEA a lansat codul sursă pentru ARC în 1986, iar ARC a fost portat pe Unix și Atari ST de Howard Chu în 1987.

Phil Katz a dezvoltat PKARC și PKXARC pentru arhivarea și extragerea fișierelor. Fișierele au funcționat cu formatul de fișier ARC și au fost semnificativ mai rapide. Spre deosebire de ARC, Katz a împărțit funcțiile de compresie și arhivare între două fișiere diferite, ceea ce a redus necesarul de memorie pentru rularea acestora.

După procesul dintre SEA și Katz, SEA s-a retras de pe piața shareware și a dezvoltat ARC+Plus cu o interfață de utilizator pe ecran complet. Formatul ARC nu mai este comun pe PC.

## Format de fișier ARC

Fișierul ARC constă dintr-o secvență de antet și fișier urmat de marcatorul de sfârșit de arhivă, așa cum se arată mai jos.

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

### Antet fișier ARC ###

|Offset|Etichetă|Tip|Valoare|Descriere|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metoda|
|02|ARCFNT|DS|12|nume fișier|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Dimensiune comprimată|
|13|ARCDAT|DW|0000|Data fișierului (MSDOS)|
|15|ARCTIM|DW|0000|Timp fișier (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Dimensiune necomprimată|
|1D|ARCFIL|DS|ARCNSZ| |

### Metode de compresie ###

Octetul metodei de compresie indică metoda de compresie utilizată. Următoarele sunt metodele de compresie utilizate pentru fișierul ARC.

|Metodă|Nume|Descriere|
|---|---|---|
|0|Stocat|Fără compresie utilizată|
|1|Ambalat|Codare repetată a lungimii de rulare (RLE)|
|2|Stors|Codare Huffman|
|3|Crunched|LZW cu buffer 4K, coduri de 12 biți|
|4|Scurcat|Prima impachetare, apoi tampon LZW 4K cu 12 biti|
|5|Cronched|Ambalare, LZW, buffer 4K, lungime variabilă (9-12 biți)|
|6|Squashed|LZW, 8K buffer, lungime variabilă (9-13 biți)|
|7|Zdrobit|Ambalare, apoi tampon LZW 8K, 2-13 biți (PAK 1.0)|
|8|Distilare|Dynamic Huffman cu tampon 8K (PAK 2.0)|

## Referințe

- [ARC (format fișier) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

