---
date: 2019-10-11
keywords: rm, .rm, format pliku rm, format pliku .rm, rozszerzenie .rm, format pliku RealMedia
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie pliku RM i interfejsach API, które umożliwiają tworzenie i otwieranie plików RM."
title: Format pliku RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Czym jest plik RM? ##

RealMedia to zastrzeżony format kontenera multimedialnego opracowany przez firmę RealNetworks, który wykorzystuje rozszerzenie .rm. Jest używany z kombinacją [RealAudio (RA)](/pl/audio/ra/) i [RealVideo(RV)](/pl/video/rv/) do przesyłania strumieniowego przez Internet. Te strumienie mają stałą przepływność. W przypadku zmiennej przepływności firma RealNetworks opracowała format RealMedia Variable Bitrate (RMVB). RealMedia nadaje się do przesyłania strumieniowego treści przez Internet i może być używany na przykład do przesyłania strumieniowego telewizji na żywo.

## Struktura pliku RealMedia ##

Plik RealMedia składa się z serii fragmentów, z których każdy ma następującą strukturę:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

W pliku RealMedia znajdują się następujące rodzaje fragmentów:

- **Nagłówek pliku RealMedia (.RMF)**: To musi być pierwsza porcja w pliku RealMedia. W jednym pliku znajduje się tylko jeden fragment RMF. Zawiera informacje o liczbie nagłówków.
- **Nagłówek właściwości pliku (PROP)**: Zawiera informacje o ogólnych właściwościach pliku RealMedia. W każdym pliku RealMedia znajduje się tylko jeden fragment tego typu.
- **Nagłówek właściwości multimediów (MDPR)**: ten fragment zawiera informacje o właściwościach strumienia. Zawiera informacje o typie strumienia i używanym kodeku. Dla każdego strumienia w pliku jest jeden fragment MDPR.
- **Nagłówek opisu treści (CONT)**: ten fragment zawiera informacje tekstowe, takie jak tytuł lub autor treści w pliku RealMedia. Ten fragment służy wyłącznie celom informacyjnym.
- **Nagłówek danych (DATA)**: Ten fragment zawiera grupę pakietów danych.
- **Nagłówek indeksu (INDX)**: Ten fragment występuje po wszystkich fragmentach DATA i zawiera wpisy indeksu. Jeden plik może mieć więcej niż jeden fragment INDX.

## Obsługiwane formaty audio i wideo ##

### Formaty audio ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
-dnet: AC3
- sipr: Sipro
- kucharz: gotować
- atrc: ATRAC3
- ralf: bezstratny format RealAudio
- raac: LC-AAC
- Racp: HE-AAC

### Formaty wideo ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: prekursor H.264
- RV40: prekursor H.264, RV40
- RVTR: H.263+ (RV20)

## Bibliografia ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

