---
date: 2019-10-11
keywords: srt, .srt, srt fájlformátum, .srt fájlformátum, .srt kiterjesztése, srt kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az SRT fájlformátumot és az API-kat, amelyek SRT-fájlokat hozhatnak létre és nyithatnak meg."
title: SRT fájlformátum
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Mi az SRT fájl? ##

Az SRT (SubRip fájlformátum) egy egyszerű feliratfájl, amely SubRip fájlformátumban van elmentve .srt kiterjesztéssel. Sorozatos számú feliratot, kezdő és befejező időbélyeget, valamint feliratszöveget tartalmaz. Az SRT-fájlok lehetővé teszik, hogy feliratokat adjunk a videótartalomhoz annak elkészítése után.

## SRT fájl szerkezete ##

Minden felirat négy részből áll az SRT fájlban.

1. Számszámláló, amely a felirat számát vagy helyét jelzi.
1. A felirat kezdési és befejezési ideje --> karakterekkel elválasztva
1. Feliratszöveg egy vagy több sorban.
1. Egy üres sor, amely a felirat végét jelzi.

### Példa az SRT-re ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Az idő megadásához *óra:perc:másodperc,ezredmásodperc (00:00:00,000)* formátumot használunk.

## SRT fájlok formázása ##

Az SRT fájlok formázása HTML címkékből származik. Az SRT-fájl formázási címkéi az alábbiakban találhatók.

| Hatás | Címkék |
| --- | --- |
|Bold|**\ <b>...\</b> ** vagy {b}...{/b}|
|Dőlt|**\ <i>...\</i> ** vagy **{i}...{/i}**|
|Aláhúzás|**\ <u>...\</u> ** vagy **{u}...{/u}**|
|Betűszín|**\ <font color="white">...\</font> **|
|Sor pozíciója|**{\a3}** (jelzi, hogy a szövegnek a 3. sorban kell megjelennie)

## SubRip szoftver ##

A SubRip egy ingyenes szoftver, amely Windows rendszeren fut. Különböző videoformátumokból kivonja a feliratokat és azok időzítését, és SRT formátumban menti a feliratokat. A SubRip optikai karakterfelismerést használ az élő videóból, más videofájlokból és DVD-kből való feliratok kinyerésére.

## Referenciák ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
