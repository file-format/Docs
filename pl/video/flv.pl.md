---
date: 2019-10-11
keywords: flv, .flv, format pliku flv, format pliku .flv, rozszerzenie .flv, rozszerzenie flv, format wideo flv
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików FLV i interfejsach API, które umożliwiają tworzenie i otwieranie plików FLV."
title: Format pliku FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Czym jest plik FLV? ##

FLV (Flash Video) to format pliku kontenera z rozszerzeniem .flv. FLV służy do dostarczania treści audio/wideo przez Internet za pomocą programu Adobe Flash Player lub Adobe Air. Dane w plikach FLV są kodowane w taki sam sposób jak pliki SWF. Bezpośrednie wsparcie zostało dodane do Flash Playera 7 w 2003 roku. Systemy Adobe stworzyły F4V w 2007 roku ze względu na ograniczenia FLV.

### Kodowanie ###

Pliki FLV zawierają strumienie bitów wideo Sorenson Spark, które są zastrzeżonym wariantem standardu wideo H.263. Jest to wymagany format kompresji dla programu Flash Player 6 i 7. Wersja 8 programu Flash Player obsługuje strumienie bitów wideo On2 TrueMotion VP6. Jest to zalecany format kompresji dla programu Flash Player 8 i nowszych wersji. FLV obsługuje dźwięk w formacie MP3, kodek Nellymoser Asao i kodek Speex typu open source. Obsługuje również nieskompresowany dźwięk lub dźwięk w formacie ADPCM. Formaty AAC (HE-AAC/AAC SBR, AAC Main Profile i AAC-LC) są obsługiwane przez najnowsze wersje programu Flash Player 9.

## Struktura ##

Pliki FLV składają się z nagłówka i pakietów. Plik FLV zaczyna się od nagłówka. Nagłówek ma następujące pola.

- **Podpis**: jego wartość to FLV
- **Wersja**: jej domyślna wartość to 1. Tylko 0x01 jest prawidłowy.
- **Flagi**: 0x04 jest używany do audio, a 0x01 do wideo, więc 0x05 jest używany zarówno do audio, jak i wideo.
- **Rozmiar nagłówka**: Wartość domyślna to 9. Służy do pomijania nowszego rozwiniętego nagłówka.

Po nagłówku następuje Pakiety. Plik FLV jest podzielony na wiele pakietów zwanych znacznikami FLV, które mają 15-bajtowe nagłówki. Pakiety zawierają metadane audio, wideo, skryptów, informacje o szyfrowaniu i ładunek. Pakiety FLV mają następujące pola.

- **Zarezerwowany**: Jest zarezerwowany dla FMS i powinien wynosić 0.
- **Filtr**: Wskazuje, czy pakiety są filtrowane, czy nie.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Typ pakietu**: Określa typ zawartości pakietu.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Rozmiar danych**: określa długość wiadomości.
- **Timestamp Lower**: Przechowuje znacznik czasu w milisekundach, w którym mają zastosowanie dane znacznika. Jest ustawiony na NULL dla pierwszego pakietu.
- **Timestamp Upper**: rozszerzenie do tworzenia wartości uint32_be.
- **Identyfikator strumienia**: jest ustawiony na NULL dla pierwszego strumienia.
- **Dane ładunku**: Są to dane oparte na typie pakietu.

## Bibliografia ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

