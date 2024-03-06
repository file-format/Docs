---
date: 2020-08-12
keywords: bpg, .bpg, bpg file format, how to open bpg files, .bpg extension, bpg extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG faila veidlapaat
linktitle: BPG
description: Lnopelniet par BPG faila formātu un API, kas var izveidot un atvērt BPG failus.
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Kas ir BPG fails? ##

BPG (Better Portable Graphics) ir faila formāts, ko Fabriss Belards 2014. gadā izveidoja digitālajiem attēliem. Viņš ierosināja BPG kā JPEG aizstājēju, jo BPG bija efektīvāks kompresijas vai izmēra ziņā. BPG izmanto HEVC (High-Efficiency Video Coding) video saspiešanas standarta iekšējā kadra kodējumu.

BPG ir izstrādāts kā pārnēsājams atmiņas ziņā efektīvs formāts darbam ar rokas un IoT ierīcēm. Pašlaik tīmekļa pārlūkprogrammas neatbalsta BPG formātu, taču vietnes joprojām var piegādāt BPG attēlus, izmantojot Bellarda rakstīto JavaScript bibliotēku. BPG izmanto HEVC galveno 4:4:4 16 Nekustīgā attēla profilu līdz 14 bitiem vienā paraugā.

## Specifikācijas ##

BPG konteinera formāts ir vispārīgs attēla formāts, nevis neapstrādāta bitu plūsma, ko izmanto HEVC. BPG atbalsta 4:4:4, 4:2:2 un 4:2:0 krāsu formātus. Alfa kanāls tiek atbalstīts arī ar atsevišķi kodētu papildu kanālu vai ceturto CMYK attēla kanālu. BPG nodrošina Exif, ICC profilu un XMP metadatu atbalstu. BPG atbalsta YCbCr (ITU-R BT.601, BT.709 un BT.2020 (nepastāvīgs spilgtums)), YCgCo, RGB, CMYK un pelēktoņu krāsu telpu. BGP atbalsta arī animāciju un zudumu un bezzudumu HEVC datu saspiešanu.

## Atsauces Nr.

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

