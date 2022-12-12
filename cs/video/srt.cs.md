---
date: 2019-10-11
keywords: srt, .srt, formát souboru srt, formát souboru .srt, přípona .srt, přípona srt
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru SRT a rozhraních API, která mohou vytvářet a otevírat soubory SRT."
title: Formát souboru SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Co je soubor SRT? ##

SRT (formát souboru SubRip) je jednoduchý soubor s titulky uložený ve formátu souboru SubRip s příponou .srt. Obsahuje sekvenční počet titulků, časová razítka začátku a konce a text titulků. Soubory SRT umožňují přidat titulky k obsahu videa po jeho vytvoření.

## Struktura souboru SRT ##

Každý titulek má v souboru SRT čtyři části.

1. Číselné počítadlo udávající číslo nebo pozici titulků.
1. Čas začátku a konce titulku oddělený znaky -->
1. Text titulků v jednom nebo více řádcích.
1. Prázdný řádek označující konec titulků.

### Příklad SRT ###

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

K určení času se používá formát *hodiny:minuty:sekundy,milisekundy (00:00:00 000)*.

## Formátování souborů SRT ##

Formátování souborů SRT je odvozeno od značek HTML. Formátovací značky pro soubor SRT jsou uvedeny níže.

| Efekt | Štítky |
| --- | --- |
|Tučné|**\ <b>...\</b> ** nebo {b}...{/b}|
|Italic|**\ <i>...\</i> ** nebo **{i}...{/i}**|
|Podtrhnout|**\ <u>...\</u> ** nebo **{u}...{/u}**|
|Barva písma|**\ <font color="white">...\</font> **|
|Pozice řádku|**{\a3}** (označuje, že text by se měl začít objevovat na řádku 3)

## Software SubRip ##

SubRip je bezplatný softwarový program, který běží na Windows. Extrahuje titulky a jejich časování z různých video formátů a ukládá je ve formátu SRT. SubRip využívá optické rozpoznávání znaků k extrahování titulků z živého videa, jiných video souborů a DVD.

## Reference ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
