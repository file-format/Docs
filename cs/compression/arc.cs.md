---
date: 2019-12-09
keywords: arc, .arc, formát souboru arc, jak otevřít soubory arc, přípona .arc, přípona arc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru ARC
linktitle: ARC
description: "Přečtěte si o formátu souboru ARC a rozhraních API, která mohou vytvářet a otevírat soubory ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Co je soubor ARC?

ARC je bezztrátový formát pro kompresi a archivaci dat vyvinutý společností System Enhancement Associates (SEA). Formát souboru a aplikace, která jej vytváří, se nazývají ARC. ARC byl velmi populární během prvních dnů vytáčeného BBS, protože kombinoval funkce komprese a archivace více souborů ve stejném souboru. ARC byl později nahrazen [ZIP](/cs/compression/zip/), který nabízel lepší kompresní poměry.

Příponu souboru .arc používá několik dalších nesouvisejících typů archivních souborů, jako je formát ARC používaný Internetovým archivem k ukládání více webových zdrojů, jiný formát ARC používaný archivátorem FreeArc, jiný formát používaný Nintendem pro zdroje atd. .

## Stručná historie formátu souborů ARC

Program ARC napsal Thom Henderson ze System Enhancement Associates v roce 1985. Tento program seskupoval soubory do jednoho archivního souboru a také je komprimoval. Soubory generované programem ARC používaly příponu .arc. SEA vydala zdrojový kód pro ARC v roce 1986 a ARC byl portován na Unix a Atari ST Howardem Chu v roce 1987.

Phil Katz vyvinul PKARC a PKXARC pro archivaci a extrahování souborů. Soubory pracovaly se souborovým formátem ARC a byly výrazně rychlejší. Na rozdíl od ARC, Katz rozdělil kompresní a archivační funkce mezi dva různé soubory, což snížilo nároky na paměť pro jejich spuštění.

Po soudním sporu mezi SEA a Katz se SEA stáhla ze sharewarového trhu a vyvinula ARC+Plus s celoobrazovkovým uživatelským rozhraním. Formát ARC již není na PC běžný.

## Formát souboru ARC

Soubor ARC se skládá ze sekvence hlavičky souboru a souboru následované značkou konce archivu, jak je uvedeno níže.

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

### Záhlaví souboru ARC ###

|Offset|Štítek|Typ|Hodnota|Popis|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metoda|
|02|ARCFNT|DS|12|název souboru|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Stlačená velikost|
|13|ARCDAT|DW|0000|Datum souboru (MSDOS)|
|15|ARCTIM|DW|0000|Čas souboru (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Nekomprimovaná velikost|
|1D|ARCFIL|DS|ARCNSZ| |

### Metody komprese ###

Bajt metody komprese označuje použitou metodu komprese. Níže jsou uvedeny metody komprese používané pro soubor ARC.

|Metoda|Název|Popis|
|---|---|---|
|0|Uloženo|Nepoužita žádná komprese|
|1|Zabaleno|Kódování opakované délky (RLE)|
|2|Stlačeno|Huffmanovo kódování|
|3|Crunched|LZW s vyrovnávací pamětí 4K, 12bitové kódy|
|4|Crunched|První balení, poté LZW 4K vyrovnávací paměť s 12 bity|
|5|Crunched|Balení, LZW, 4K vyrovnávací paměť, proměnná délka (9-12 bitů)|
|6|Squashed|LZW, 8K vyrovnávací paměť, proměnná délka (9-13 bitů)|
|7|Crushed|Packing, pak LZW 8K buffer, 2-13 bitů (PAK 1.0)|
|8|Destilovat|Dynamický Huffman s 8K pufrem (PAK 2.0)|

## Reference

- [ARC (formát souboru) - Wikipedie](https://en.wikipedia.org/wiki/ARC_(file_format))

