---
date: 2020-08-12
keywords: bpg, .bpg, formát souboru bpg, jak otevřít soubory bpg, přípona .bpg, přípona bpg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru BPG
linktitle: BPG
description: "Přečtěte si o formátu souborů BPG a rozhraních API, která mohou vytvářet a otevírat soubory BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Co je soubor BPG? ##

BPG (Better Portable Graphics) je souborový formát vytvořený Fabricem Bellardem v roce 2014 pro digitální obrázky. Navrhl BPG jako náhradu za JPEG, protože BPG bylo efektivnější z hlediska komprese nebo velikosti. BPG používá kódování uvnitř snímku podle standardu komprese videa HEVC (High-Efficiency Video Coding).

BPG je navržen jako přenosný paměťově efektivní formát pro práci na kapesních a IoT zařízeních. V současné době webové prohlížeče nepodporují formát BPG, ale webové stránky mohou stále dodávat obrázky BPG pomocí knihovny JavaScript napsané Bellardem. BPG používá profil HEVC Main 4:4:4 16 Still Picture až do 14 bitů na vzorek.

## Specifikace ##

Formát kontejneru BPG je obecný formát obrázku spíše než nezpracovaný bitstream používaný v HEVC. BPG podporuje barevné formáty 4:4:4, 4:2:2 a 4:2:0. Alfa kanál je také podporován se samostatně kódovaným extra kanálem nebo čtvrtým kanálem obrazu CMYK. BPG poskytuje podporu metadat pro Exif, ICC profily a XMP. BPG podporuje YCbCr (ITU-R BT.601, BT.709 a BT.2020 (nekonstantní jas)), YCgCo, RGB, CMYK a barevný prostor ve stupních šedi. BGP také podporuje animaci a ztrátovou a bezztrátovou kompresi dat HEVC.

## Reference ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

