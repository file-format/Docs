---
date: 2020-08-12
keywords: bpg, .bpg, bpg file format, how to open bpg files, .bpg extension, bpg extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG failo formaat
linktitle: BPG
description: Luždirbti apie BPG failo formatą ir API, kurios gali sukurti ir atidaryti BPG failąs.
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Kas yra BPG failas? ##

BPG (Better Portable Graphics) yra failo formatas, kurį 2014 m. sukūrė Fabrice'as Bellard skaitmeniniams vaizdams. Jis pasiūlė BPG kaip JPEG pakaitalą, nes BPG buvo veiksmingesnis suspaudimo ar dydžio efektyvumu. BPG naudoja HEVC (High-Efficiency Video Coding) vaizdo glaudinimo standarto vidinio kadro kodavimą.

BPG sukurtas kaip nešiojamas atmintį taupantis formatas, skirtas dirbti delniniuose ir daiktų interneto įrenginiuose. Šiuo metu žiniatinklio naršyklės nepalaiko BPG formato, tačiau svetainės vis tiek gali pateikti BPG vaizdus, naudodamos Bellard parašytą JavaScript biblioteką. BPG naudoja HEVC pagrindinį 4:4:4 16 Nejudančio vaizdo profilį iki 14 bitų vienam pavyzdžiui.

## Specifikacijos ##

BPG konteinerio formatas yra bendras vaizdo formatas, o ne neapdorotas bitų srautas, naudojamas HEVC. BPG palaiko 4:4:4, 4:2:2 ir 4:2:0 spalvų formatus. Alfa kanalas taip pat palaikomas atskirai užkoduotu papildomu kanalu arba ketvirtuoju CMYK vaizdo kanalu. BPG teikia Exif, ICC profilių ir XMP metaduomenų palaikymą. BPG palaiko YCbCr (ITU-R BT.601, BT.709 ir BT.2020 (nepastovus šviesumas)), YCgCo, RGB, CMYK ir pilkos spalvos spalvų erdvę. BGP taip pat palaiko animaciją ir nuostolingą bei be nuostolių HEVC duomenų glaudinimą.

## Nuorodos Nr.

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

