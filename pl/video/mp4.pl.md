---
date: 2019-10-11
keywords: MP4, plik, rozszerzenie, format, format wideo, MPEG-4
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików MP4 i interfejsach API, które umożliwiają tworzenie i otwieranie plików MP4."
title: Format pliku MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Co to jest plik MP4? ##

MP4 (skrót od MPEG-4 Part 14) to format pliku oparty na normie ISO/IEC 14496-12:2004, który jest oparty na formacie plików QuickTime, ale formalnie określa obsługę początkowych deskryptorów obiektów (IOD) i innych funkcji MPEG. Jest używany głównie do przechowywania wideo i audio, ale może być również używany do przechowywania napisów i zdjęć. Pliki MP4 są przechowywane z rozszerzeniem .mp4. MP4 to międzynarodowy standard kodowania audiowizualnego. Podobnie jak większość nowoczesnych formatów kontenerów, MP4 obsługuje przesyłanie strumieniowe przez Internet. Ze względu na wysoką kompresję stosowaną w MP4, wynikowe pliki są mniejsze i zachowują prawie całą oryginalną jakość.

## Krótka historia ##

Specyfikacja MP4 została opracowana przez Moving Picture Experts Group (MPEG) i była oparta na formacie QuickTime [MOV](/pl/video/mov/), który został opublikowany w 2001 roku. Pierwsza wersja (ISO/IEC 14496-1:2001) MP4 była wersją MPEG-4 Part 1: Specyfikacja systemów opublikowaną w 1999 roku. Format pliku MP4 został uogólniony do ISO Base Media File Format ISO / IEC 14496-12: 2004, który definiuje ogólną strukturę plików multimedialnych opartych na czasie. W rezultacie jest używany jako podstawa dla innych formatów plików.

## Struktura plików MP4 ##

MP4 to rozszerzalny plik kontenera, co oznacza, że nie definiuje ścisłej struktury i umożliwia niestandardową strukturę i hierarchię dla każdego typu multimediów. Dane w pliku MP4 są podzielone na dwie sekcje, pierwsza zawiera dane związane z mediami, a druga zawiera metadane. Dane multimedialne zawierają audio lub wideo, a metadane wskazują flagi dostępu swobodnego, znaczniki czasu itp.
Struktury w MP4 są zwykle określane jako atomy lub pudełka. Minimalny rozmiar atomu to 8 bajtów (pierwsze 4 bajty określają rozmiar, a kolejne 4 bajty określają typ). Oto lista atomów poziomu głównego zawartych w plikach MP:

- **ftyp**: Zawiera typ pliku, opis i używane wspólne struktury danych.
- **pdin**: zawiera informacje o progresywnym ładowaniu/pobieraniu wideo.
- **moov**: Pojemnik na wszystkie metadane filmu.
- **moof**: Pojemnik z fragmentami wideo.
- **mfra**: Kontener z losowym dostępem do fragmentu wideo
- **mdat**: Kontener danych dla multimediów.
- **stts**: tabela od próbki do czasu.
- **stsc**: tabela próbka-kawałek.
- **stsz**: przykładowe rozmiary (ramki)
- **meta**: kontener z informacjami o metadanych.

Oto lista atomów drugiego poziomu używanych w MP4:

- **mvhd**: Zawiera informacje nagłówka wideo z pełnymi szczegółami wideo.
- **trak**: Kontener z indywidualnym torem.
- **udta**: Kontener z informacjami o użytkowniku i utworze.
- **iods**: deskryptor pliku MP4

## Bibliografia ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

