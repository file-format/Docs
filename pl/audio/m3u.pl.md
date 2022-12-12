---
date: 2019-12-13
keywords: m3u, format pliku m3u, rozszerzenie .m3u, multimedialna lista odtwarzania m3u, format listy odtwarzania m3u
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików M3U i interfejsach API, które umożliwiają tworzenie i otwieranie plików M3U."
title: Format pliku M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Czym jest plik M3U? ##

M3U (URL MP3) to plik listy odtwarzania audio przechowywany z rozszerzeniem .m3u. M3U nie jest rzeczywistym plikiem audio, po prostu wskazuje na pliki audio, a czasem wideo. M3U został opracowany do użytku z oprogramowaniem Winplay3 firmy Fraunhofer. Jest również obsługiwany przez różne odtwarzacze multimedialne i oprogramowanie.

## Format pliku M3U

Nie ma oficjalnej specyfikacji formatu pliku M3U, jest to de facto standard. M3U to zwykły plik tekstowy, który używa rozszerzenia .m3u, jeśli tekst jest zakodowany w domyślnym kodowaniu systemu lokalnego innym niż Unicode lub z rozszerzeniem .m3u8, jeśli tekst jest zakodowany w UTF-8. Każdy wpis w pliku M3U może być jednym z następujących:

- Bezwzględna ścieżka do pliku
- Ścieżka pliku względem pliku M3U.
- Adres URL

### Rozszerzony M3U ###

W rozszerzonym M3U wprowadzono dodatkowe dyrektywy, które zaczynają się od „#” i kończą dwukropkiem (:), jeśli mają parametry. Poniżej podano listę dyrektyw dla rozszerzonego M3U.

- **#EXTM3U** - Jest to nagłówek pliku wskazujący rozszerzone M3U i musi być pierwszym wierszem pliku.
- **#EXTENC:** - Kodowanie tekstu. Musi to być druga linia pliku.
- **#EXTINF:** - Używany do informacji o utworze i innych dodatkowych właściwości.
- **#PLAYLIST:** - Tytuł listy odtwarzania
- **#EXTGRP:** - Rozpocznij grupowanie nazw
- **#EXTALB:** - Informacje o albumie
- **#EXTART:** - Artysta albumu
- **#EXTGENRE** - Gatunek albumu
- **#EXTM3A** - Pojedyncza lista odtwarzania dla utworów z albumu lub rozdziałów.
- **#EXTBYT:** - Rozmiar pliku w bajtach.
- **#EXTBIN:** - Następują dane binarne.
- **#EXTIMG:** - Logo, okładka lub inne obrazy.

### HLS M3U ###

HLS (HTTP Live Streaming) został stworzony przez firmę Apple w celu strumieniowego przesyłania dźwięku i radia na urządzenia z systemem iOS. Opiera się na rozszerzonym M3U zakodowanym w UTF-8. Został znormalizowany jako RFC 8216 w 2017 roku przez IETF. Tagi listy odtwarzania HLS zaczynają się od „#EXT-X-”. Poniżej podano listę tagów dla HLS

- **EXT-X-VERSION** — wskazuje wersję zgodności pliku na podstawie nośnika i jego serwera.
- **#EXT-X-START:** — wskazuje preferowany punkt początkowy listy odtwarzania.
- **#EXT-X-PLAYLIST-TYPE:** - Podaje typ listy odtwarzania (EVENT lub VOD).
- **#EXT-X-TARGETDURATION:** - Określa maksymalny czas trwania Segmentu.
- **#EXT-X-MEDIA-SEQUENCE:** - Wskazuje numer sekwencji nośnika.
- **#EXT-X-INDEPENDENT-SEGMENTS** — wskazuje, że wszystkie próbki multimediów są niezależne i mogą być dekodowane bez innych segmentów.
- **#EXT-X-MEDIA:** - Służy do łączenia list odtwarzania multimediów, które zawierają alternatywne wersje tej samej treści.
- **#EXT-X-STREAM-INF:** - Określa strumień wariantów, który jest częścią wersji.
- **#EXT-X-BYTERANGE:** — wskazuje, że segment multimediów jest podzakresem zasobu identyfikowanego przez jego identyfikator URI.
- **#EXT-X-DISCONTINUITY** — wskazuje na brak ciągłości między poprzedzającymi i kolejnymi segmentami mediów.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Umożliwia synchronizację między różnymi wersjami tego samego strumienia wariantów lub różnych strumieni wariantów.
- **#EXT-X-KEY:** - Określa sposób odszyfrowywania segmentów multimediów.
- **#EXT-X-MAP:** - Określa, jak uzyskać sekcję inicjalizacji nośnika. Wymagane jest przeanalizowanie odpowiednich segmentów mediów.
- **#EXT-X-PROGRAM-DATE-TIME:** - Wiąże pierwszą próbkę Segmentu Mediów z bezwzględną datą i/lub godziną.
- **#EXT-X-DATERANGE:** - Łączy zakres danych.
- **#EXT-XI-FRAMES-ONLY** — wskazuje, że każdy segment multimediów na liście odtwarzania opisuje pojedynczą ramkę I.
- **EXT-XI-FRAME-STREAM-INF** - Wskazuje, że plik listy odtwarzania zawiera I-ramki prezentacji multimedialnej.
- **#EXT-X-SESSION-DATA:** - Umożliwia przechowywanie dowolnych danych sesji
przenoszone na głównej liście odtwarzania.
- **#EXT-X-SESSION-KEY:** - Pozwala na szyfrowanie kluczy. Klient może wstępnie załadować te klucze bez uprzedniego odczytywania listy odtwarzania.
- **#EXT-X-ENDLIST** — wskazuje, że do pliku nie zostaną dodane żadne segmenty multimediów.

Poniżej znajduje się lista typów mediów internetowych używanych przez M3U:

- **application/vnd.apple.mpegurl**: Jest to jedyny zarejestrowany typ multimediów (zarejestrowany w 2009 r.) dla M3U, który jest używany do odwoływania się do list odtwarzania w aplikacjach HLS.
- Następujące typy mediów internetowych są używane przez aplikacje inne niż HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Przykład M3U ##

To jest przykład pliku M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Bibliografia ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Przesyłanie strumieniowe HTTP na żywo](https://tools.ietf.org/html/rfc8216)

