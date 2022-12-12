---
date: 2019-10-11
keywords: f4v, .f4v, format pliku f4v, format pliku .f4v, rozszerzenie .f4v, rozszerzenie f4v, format wideo f4v, jak otwierać pliki f4v, co to są pliki f4v
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików F4V i interfejsach API, które umożliwiają tworzenie i otwieranie plików F4V"
title: Format pliku F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Czym jest plik F4V? ##

F4V (Flash MP4 Video File) to plik wideo zapisany z rozszerzeniem .f4v. Opiera się na podstawowym formacie plików multimedialnych ISO (MPEG-4 Part 12). Jest bardzo podobny do [MP4](/pl/video/mp4/), dlatego nieformalnie jest również nazywany Flash MP4. [FLV](/pl/video/flv/) miał ograniczenia podczas przesyłania strumieniowego zawartości H.264/ACC, co spowodowało, że firma Adobe Systems stworzyła nowy format F4V. Flash Player może odtwarzać pliki F4V od czasu wydania Flash Player 9 Update 3.

## Struktura plików F4V ##

Format pliku F4V jest oparty na podstawowym formacie plików multimedialnych ISO (MPEG-4 część 12) i jest bardzo podobny do formatu MP4. Szczegółowe informacje dotyczące struktury można znaleźć na stronie [MP4](/pl/video/mp4/). Główną różnicą między F4V i MP4 są formaty metadanych, które może przechowywać F4V. Poniżej podano listę formatów metadanych obsługiwanych przez format F4V.

- **Pole tagów**: Dodatkowe cztery opcjonalne pola tagów (auth, title, dscp, cprt) w polu Movie (moov).
- **Okno metadanych XMP**: To pole pojawia się zaraz po polu Film (moov). Dzięki temu plik może przekazywać metadane XMP do filmu SWF za pośrednictwem języka ActionScript.
- **ilst box**: To pole występuje wewnątrz pola Meta (meta) i może zawierać wiele tagów metadanych. Obsługiwane typy danych podano poniżej.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Okno metadanych ścieżki tekstowej**: próbki tekstu (text lub tx3g) w Media Databox (mdat). Może zawierać następujące pola metadanych.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Bibliografia ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

