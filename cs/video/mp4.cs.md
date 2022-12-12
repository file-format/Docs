---
date: 2019-10-11
keywords: MP4, soubor, přípona, formát, video formát, MPEG-4
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souborů MP4 a rozhraních API, která mohou vytvářet a otevírat soubory MP4."
title: Formát souboru MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Co je soubor MP4? ##

MP4 (zkratka pro MPEG-4 Part 14) je formát souboru založený na ISO/IEC 14496-12:2004, který je založen na formátu QuickTime File Format, ale formálně specifikuje podporu pro Initial Object Descriptors (IOD) a další funkce MPEG. Většinou se používá k ukládání videa a zvuku, ale lze jej použít také k ukládání titulků a statických obrázků. Soubory MP4 jsou uloženy s příponou .mp4. MP4 je mezinárodní standard audio-vizuálního kódování. Podobně jako většina moderních formátů kontejnerů podporuje MP4 streamování přes internet. Díky vysoké kompresi použité v MP4 jsou výsledné soubory menší velikosti a téměř veškerá původní kvalita je zachována.

## Stručná historie ##

Specifikace MP4 byla vyvinuta Moving Picture Experts Group (MPEG) a byla založena na formátu QuickTime [MOV](/cs/video/mov/), který byl publikován v roce 2001. První verze (ISO/IEC 14496-1:2001) MP4 byla revize specifikace MPEG-4 Part 1: Systems publikovaná v roce 1999. Formát souboru MP4 byl zobecněn na ISO Base Media File Format ISO/IEC 14496-12:2004, která definovala obecnou strukturu pro časově založené mediální soubory. V důsledku toho se používá jako základ pro jiné formáty souborů.

## Struktura souborů MP4 ##

MP4 je rozšiřitelný kontejnerový soubor, což znamená, že nedefinuje striktní strukturu a umožňuje vlastní strukturu a hierarchii pro každý typ média. Data v souboru MP4 jsou rozdělena do dvou částí, první obsahuje data související s médiem a druhá obsahuje metadata. Mediální data obsahují zvuk nebo video a metadata označují příznaky náhodného přístupu, časová razítka atd.
Struktury v MP4 se typicky označují jako atomy nebo krabice. Minimální velikost atomu je 8 bajtů (první 4 bajty určují velikost a další 4 bajty typ). Zde je seznam atomů kořenové úrovně obsažených v souborech MP:

- **ftyp**: Obsahuje typ souboru, popis a běžné používané datové struktury.
- **pdin**: Obsahuje informace o postupném načítání/stahování videa.
- **moov**: Kontejner pro všechna metadata filmu.
- **moof**: Kontejner s fragmenty videa.
- **mfra**: Kontejner s náhodným přístupem k fragmentu videa
- **mdat**: Datový kontejner pro média.
- **stts**: tabulka mezi vzorky a časem.
- **stsc**: tabulka mezi vzorky.
- **stsz**: velikosti vzorku (rámování)
- **meta**: Kontejner s informacemi o metadatech.

Zde je seznam atomů druhé úrovně používaných v MP4:

- **mvhd**: Obsahuje informace v záhlaví videa s úplnými podrobnostmi o videu.
- **trak**: Kontejner s jednotlivou stopou.
- **udta**: Kontejner s informacemi o uživateli a stopě.
- **iods**: deskriptor souboru MP4

## Reference ##

- [MP4 - Wikipedie](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

