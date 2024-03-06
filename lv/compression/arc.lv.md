---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC faila veidlapaat
linktitle: ARC
description: Lnopelniet par ARC faila formātu un API, kas var izveidot un atvērt ARC failus.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Kas ir ARC fails?

ARC ir bezzudumu datu saspiešanas un arhivēšanas formāts, ko izstrādājis System Enhancement Associates (SEA). Gan faila formātu, gan lietojumprogrammu, kas to izveido, sauc par ARC. ARC bija ļoti populārs iezvanpieejas BBS pirmsākumos, jo tas apvienoja saspiešanas un vairāku failu arhivēšanas funkcijas vienā failā. Vēlāk ARC tika aizstāts ar [ZIP](/compression/zip/), kas piedāvāja labākus saspiešanas koeficientus.

Faila paplašinājumu .arc izmanto vairāki citi nesaistīti arhīva failu tipi, piemēram, ARC formāts, ko izmanto interneta arhīvs, lai saglabātu vairākus tīmekļa resursus, cits ARC formāts, ko izmanto FreeArc arhivētājs, cits formāts, ko Nintendo izmanto resursiem utt. .

## Īsa ARC faila formāta vēsture

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Šī programma grupēja failus vienā arhīva failā un arī saspieda tos. Programmas ARC ģenerētajos failos tika izmantots paplašinājums .arc. SEA izlaida ARC pirmkodu 1986. gadā, un Hovards Ču 1987. gadā ARC pārnesa uz Unix un Atari ST.

Fils Katzs izstrādāja PKARC un PKXARC failu arhivēšanai un izvilkšanai. Faili darbojās ar ARC faila formātu un bija ievērojami ātrāki. Atšķirībā no ARC, Katz sadalīja saspiešanas un arhivēšanas funkcijas starp diviem dažādiem failiem, kas samazināja atmiņas nepieciešamību to palaišanai.

Pēc tiesas prāvas starp SEA un Katz, SEA izstājās no shareware tirgus un izstrādāja ARC+Plus ar pilnekrāna lietotāja interfeisu. ARC formāts vairs nav izplatīts datorā.

## ARC faila formāts

ARC fails sastāv no faila galvenes un faila secības, kam seko arhīva beigu marķieris, kā parādīts tālāk.

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

### ARC faila galvene ###

|Nobīde|Etiķete|Tips|Vērtība|Apraksts|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metode|
|02|ARCFNT|DS|12|faila nosaukums|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Saspiests izmērs|
|13|ARCDAT|DW|0000|Faila datums (MSDOS)|
|15|ARCTIM|DW|0000|Faila laiks (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Nesaspiests izmērs|
|1D|ARCFIL|DS|ARCNSZ| |

### Saspiešanas metodes ###

Saspiešanas metodes baits norāda izmantoto saspiešanas metodi. Tālāk ir norādītas ARC failam izmantotās saspiešanas metodes.

|Metode|Nosaukums|Apraksts|
|---|---|---|
|0|Saglabāts|Nav izmantota kompresija|
|1|Iepakots|Atkārtota darbības garuma kodējums (RLE)|
|2|Saspiests|Huffman kodējums|
|3|Crunched|LZW ar 4K buferi, 12 bitu kodi|
|4|Crunched|Vispirms iepakojums, pēc tam LZW 4K buferis ar 12 bitiem|
|5|Crunched|Iepakojums, LZW, 4K buferis, mainīgs garums (9–12 biti)|
|6|Saspiests|LZW, 8K buferis, mainīgs garums (9–13 biti)|
|7|Sasmalcināts|Iesaiņojums, pēc tam LZW 8K buferis, 2–13 biti (PAK 1.0)|
|8|Distill|Dynamic Huffman ar 8K buferi (PAK 2.0)|

## Atsauces

- [ARC (file format) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

