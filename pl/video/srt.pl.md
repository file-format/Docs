---
date: 2019-10-11
keywords: srt, .srt, format pliku srt, format pliku .srt, rozszerzenie .srt, rozszerzenie srt
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików SRT i interfejsach API, które umożliwiają tworzenie i otwieranie plików SRT."
title: Format pliku SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Czym jest plik SRT? ##

SRT (format pliku SubRip) to prosty plik napisów zapisany w formacie pliku SubRip z rozszerzeniem .srt. Zawiera sekwencyjną liczbę napisów, znaczniki czasu rozpoczęcia i zakończenia oraz tekst napisów. Pliki SRT umożliwiają dodawanie napisów do treści wideo po ich wyprodukowaniu.

## Struktura pliku SRT ##

Każdy napis ma cztery części w pliku SRT.

1. Licznik numeryczny wskazujący numer lub pozycję napisów.
1. Czas rozpoczęcia i zakończenia napisów oddzielone znakami -->
1. Tekst napisów w jednym lub kilku wierszach.
1. Pusta linia oznaczająca koniec napisów.

### Przykład SRT ###

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

Do określenia czasu używany jest format *godziny:minuty:sekundy, milisekundy (00:00:00,000)*.

## Formatowanie plików SRT ##

Formatowanie plików SRT wywodzi się ze znaczników HTML. Poniżej wymieniono znaczniki formatowania pliku SRT.

| Efekt | Tagi |
| --- | --- |
|Pogrubienie|**\ <b>...\</b> ** lub {b}...{/b}|
|Kursywa|**\ <i>...\</i> ** lub **{i}...{/i}**|
|Podkreśl|**\ <u>...\</u> ** lub **{u}...{/u}**|
|Kolor czcionki|**\ <font color="white">...\</font> **|
|Pozycja wiersza|**{\a3}** (wskazuje, że tekst powinien zacząć pojawiać się w wierszu 3)

## Oprogramowanie SubRip ##

SubRip to darmowy program działający w systemie Windows. Wyodrębnia napisy i ich czasy z różnych formatów wideo i zapisuje napisy w formacie SRT. SubRip wykorzystuje optyczne rozpoznawanie znaków do wyodrębniania napisów z wideo na żywo, innych plików wideo i płyt DVD.

## Bibliografia ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
