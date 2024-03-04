---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC failo formaat
linktitle: ARC
description: Luždirbti apie ARC failo formatą ir API, kurios gali sukurti ir atidaryti ARC failąs.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Kas yra ARC failas?

ARC yra nenuostolingas duomenų glaudinimo ir archyvavimo formatas, kurį sukūrė System Enhancement Associates (SEA). Failo formatas ir jį kurianti programa vadinami ARC. ARC buvo labai populiarus pirmosiomis telefono ryšio BBS dienomis, nes sujungė kelių failų glaudinimo ir archyvavimo funkcijas tame pačiame faile. Vėliau ARC buvo pakeistas [ZIP](/compression/zip/), kuris pasiūlė geresnį suspaudimo laipsnį.

.arc failo plėtinį naudoja keli kiti nesusiję archyvo failų tipai, pvz., ARC formatas, naudojamas interneto archyve, kad būtų saugomi keli žiniatinklio ištekliai, kitas ARC formatas, naudojamas FreeArc archyvavimo priemonėje, kitas formatas, naudojamas Nintendo ištekliams ir kt. .

## Trumpa ARC failo formato istorija

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Ši programa sugrupavo failus į vieną archyvo failą ir taip pat juos suglaudino. ARC programos sugeneruoti failai naudojo .arc plėtinį. SEA išleido ARC šaltinio kodą 1986 m., o ARC į Unix ir Atari ST perkėlė Howardas Chu 1987 m.

Philas Katzas sukūrė PKARC ir PKXARC failams archyvuoti ir išgauti. Failai veikė ARC failo formatu ir buvo žymiai greitesni. Skirtingai nei ARC, Katzas suspaudimo ir archyvavimo funkcijas padalijo tarp dviejų skirtingų failų, todėl sumažėjo atminties poreikis jiems paleisti.

Po ieškinio tarp SEA ir Katz, SEA pasitraukė iš shareware rinkos ir sukūrė ARC+Plus su viso ekrano vartotojo sąsaja. ARC formatas nebėra įprastas asmeniniame kompiuteryje.

## ARC failo formatas

ARC failą sudaro failo antraštės ir failo seka, po kurios eina archyvo pabaigos žymeklis, kaip parodyta toliau.

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

### ARC failo antraštė ###

|Poslinkis|Etiketė|Tipas|Vertė|Aprašymas|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metodas|
|02|ARCFNT|DS|12|failo pavadinimas|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Suspaustas dydis|
|13|ARCDAT|DW|0000|Failo data (MSDOS)|
|15|ARCTIM|DW|0000|Failo laikas (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Nesuspaustas dydis|
|1D|ARCFIL|DS|ARCNSZ| |

### Suspaudimo metodai ###

Suspaudimo metodo baitas nurodo naudojamą glaudinimo metodą. Toliau pateikiami ARC failo glaudinimo metodai.

|Metodas|Pavadinimas|Aprašymas|
|---|---|---|
|0|Saugoma|Suspaudimas nenaudojamas|
|1|Supakuota|Pakartotinio veikimo ilgio kodavimas (RLE)|
|2|Suspaustas|Huffmano kodavimas|
|3|Crunched|LZW su 4K buferiu, 12 bitų kodais|
|4|Sutraiškytas|Pirmiausia įpakavimas, tada LZW 4K buferis su 12 bitų|
|5|Sutraiškytas|Įpakavimas, LZW, 4K buferis, kintamo ilgio (9–12 bitų)|
|6|Suspaustas|LZW, 8K buferis, kintamo ilgio (9–13 bitų)|
|7|Susmulkintas|Įpakavimas, tada LZW 8K buferis, 2–13 bitų (PAK 1.0)|
|8|Distiliuoti|Dynamic Huffman su 8K buferiu (PAK 2.0)|

## Nuorodos

- [ARC (file format) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

