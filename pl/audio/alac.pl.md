---
date: 2021-03-21
keywords: alac, format pliku alac, rozszerzenie .alac
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików ALAC i interfejsach API, które mogą tworzyć i otwierać pliki ALAC."
title: ALAC — Apple Lossless Audio Codec Format pliku
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Czym jest plik ALAC?

Format pliku ALAC to Apple Lossless Audio Codec (ALAC), który wykorzystuje kontener QuickTime zgodny z MPEG-4. Został wprowadzony w 2004 roku jako zastrzeżony format pliku, aż do 2011 roku, kiedy Apple udostępnił go jako open source i nieodpłatnie. Format jest podobny do [FLAC](/pl/audio/flac/) (bezstratny bezstratny kodek audio), ale oferuje stosunkowo większą kompresję. Oferuje lepiej brzmiącą alternatywę dla [AAC](/pl/audio/aac/) lub [MP3](/pl/audio/mp3/). Pliki audio zakodowane za pomocą kodeka ALAC można otwierać za pomocą Apple QuickTime, Apple iTunes i Micrsoft Windows Media Player z kodekiem K-Lite.

## Format pliku ALAC

Pliki oparte na kodeku ALAC to pliki binarne, które są dostępne jako [open source na GitHub](https://github.com/macosforge/alac) w celach informacyjnych dla programistów. Zawiera źródła dla kodera i dekodera ALAC. Firma Apple udostępniła również narzędzie wiersza poleceń o nazwie `alacconvert`, które umożliwia odczytywanie i zapisywanie danych audio do/z plików Core Audio Format (CAF) i [WAVE](/pl/audio/wav/). Poniżej przedstawiono kilka kluczowych punktów dotyczących formatu pliku ALAC.

1. „Głębia bitowa” - 16, 20, 24 i 32 bity.
1. „Częstotliwość próbkowania” — Dowolna częstotliwość próbkowania w zakresie od 1 do 384 000 Hz. Obsługiwane mogą być częstotliwości teoretyczne do 4 294 967 295 (2^32 - 1) Hz.
1. `Packet Size` - Domyślny rozmiar pakietu to 4096 przykładowych ramek audio na pakiet. Z pewnością możliwe są inne rozmiary pakietów. Jednak pakiety o innych niż domyślne rozmiarach nie gwarantują prawidłowego działania na wszystkich urządzeniach obsługujących technologię Apple Lossless. Pakiety powyżej 16 384 przykładowych ramek nie są obsługiwane.
1. „Obsługiwane kanały” — obsługuje od jednego do ośmiu kanałów. Każdy kanał ma następującą kolejność informacji.

|Num Chan| Zamów|
|---|---|
|1 |mono|
|2 |stereo (lewy, prawy)|
|3 |MPEG 3.0 B (środek, lewa, prawa)|
|4 |MPEG 4.0 B (środek, lewy, prawy, środkowy dźwięk przestrzenny)|
|5 |MPEG 5.0 D (środek, lewy, prawy, lewy dźwięk przestrzenny, prawy dźwięk przestrzenny)|
|6 |MPEG 5.1 D (środek, lewy, prawy, lewy dźwięk przestrzenny, prawy dźwięk przestrzenny, efekty niskiej częstotliwości)|
|7 |Apple AAC 6.1 (środek, lewy, prawy, lewy dźwięk przestrzenny, prawy dźwięk przestrzenny, środkowy dźwięk przestrzenny, efekty niskich częstotliwości)|
|8 |MPEG 7.1 B (środek, lewy środek, prawy środek, lewy, prawy, lewy dźwięk przestrzenny, prawy dźwięk przestrzenny, efekty niskiej częstotliwości)|

## Bibliografia

* [ALAC – Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)
* [macosforge - alac na GitHub](https://github.com/macosforge/alac)

