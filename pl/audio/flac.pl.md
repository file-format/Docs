---
date: 2019-12-13
keywords: flac, format pliku flac, rozszerzenie .flac, plik flac, flac vs mp3
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików FLAC i interfejsach API, które umożliwiają tworzenie i otwieranie plików FLAC."
title: Format pliku FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Czym jest plik FLAC?

FLAC (Free Lossless Audio Codec) to bezstratny format kodowania dźwięku z kompresją opracowany przez Fundację Xiph.Org. FLAC to wolny od tantiem otwarty format, który jest zapisywany z rozszerzeniem .flac. Cyfrowy dźwięk skompresowany przy użyciu algorytmu FLAC jest zwykle zmniejszany do rozmiaru od 50 do 70 procent. Pliki FLAC można rozpakować do identycznej kopii oryginalnych plików audio.

## Format pliku FLAC

To jest przegląd strumienia bitów FLAC.

- **fLaC marker**: Ten znacznik jest dodawany na początku strumienia. Po nim następuje jeden lub więcej bloków metadanych.
- **Bloki metadanych**: FLAC obsługuje 128 rodzajów bloków metadanych; obecnie zdefiniowane są następujące.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **RAMKA**: Dane audio składają się z jednej lub więcej ramek audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Krótka historia formatu plików FLAC

Josh Coalson rozpoczął rozwój FLAC w 2000 r. Pierwsza wersja FLAC została wydana 20 lipca 2001 r. FLAC został włączony pod flagą Xiph.Org 20 stycznia 2003 r. Rozwój FLAC został przeniesiony do Xiph.Org repozytorium git z wydanie wersji 1.3.0 w dniu 26 marca 2013 r.

## Skład projektu FLAC

Projekt FLAC składa się z następujących elementów:

- Formaty strumieniowe.
- Prosty format kontenera dla strumienia (FLAC).
- libFLAC: Biblioteka referencyjnych koderów, dekoderów i interfejsu metadanych.
- libFLAC++: zorientowane obiektowo opakowanie dla libFLAC.
- flac: Program wiersza poleceń do kodowania i dekodowania strumieni FLAC.
- metaflac: Edytor metadanych z wiersza poleceń dla FLAC.
- Wtyczki wejściowe dla odtwarzaczy muzycznych, takich jak Winamp, XMMX itp.
- Format kontenera Ogg (Ogg FLAC).

## Projekt FLACa

W zależności od gęstości i amplitudy muzyki rozmiar skompresowanego pliku może być o 80% mniejszy niż oryginalny plik.

### Koder źródła ###

- Obsługuje tylko próbki całkowite, a nie zmiennoprzecinkowe. Może obsługiwać rozdzielczość bitową PCM od 4 do 32 bitów na próbkę i częstotliwość próbkowania od 1 Hz do 65 535 Hz. Kodowanie FLAC jest ograniczone do 24 bitów na próbkę.
- Kanały można grupować w celu wykorzystania korelacji międzykanałowych w celu zwiększenia kompresji.
- Sumy kontrolne CRC służą do identyfikacji uszkodzonych ramek.
- Do konwersji próbek audio FLAC wykorzystuje predykcję liniową.

### Metadane ###

- FLAC obsługuje ReplayGain (używany do postrzegania i normalizacji głośności w dźwięku).
- FLAC używa tego samego systemu, który jest używany w komentarzach Vorbisa do tagowania.
- libFLAC jest używany przez większość aplikacji FLAC do kodowania/dekodowania.
- API libFLAC jest zorganizowane w strumienie, strumienie z możliwością wyszukiwania i pliki w celu zwiększenia abstrakcji od podstawowego strumienia bitów FLAC.

### Kompresja ###

libFLAC używa poziomów kompresji od 0 do 8, gdzie 0 to najszybszy, a 8 to najwolniejszy poziom kompresji. Skompresowane pliki są zawsze bezstratne, chociaż kompromis jest między szybkością a rozmiarem.

## FLAC kontra MP3
MP3 to format kompresji stratnej, co oznacza, że po zastosowaniu kompresji może wyciąć część dźwięku, aby zmniejszyć jego rozmiar. Natomiast FLAC to bezstratny format pliku, co oznacza, że możesz usłyszeć dźwięk w najczystszej postaci. Wcześniej bezstratnymi formatami plików były CDA lub WAV, które nie były tak wydajne jak FLAC. Poniższa tabela przedstawia porównanie tych dwóch formatów dla niektórych ważnych terminów:

|Termin|FLAC|MP3|
---|---|---|
|**Jakość danych**|Brak utraty danych audio| Niektóre dane mogą zostać utracone podczas kompresji danych audio|
|**Rozmiar**|Większy rozmiar pliku w porównaniu do formatów stratnych. Potrzebujesz więc większej pojemności pamięci masowej| Mniejszy rozmiar pliku, odpowiedni do odtwarzania na kompaktowych urządzeniach audio z niewielką ilością miejsca do przechowywania |
|**Wymagania sprzętowe**| Potrzebujesz wysokiej jakości sprzętu audio i dużej pojemności | Ogromne biblioteki audio można zapisać na mniejszej przestrzeni dyskowej. Nadaje się do urządzeń przenośnych, takich jak odtwarzacze audio lub telefony komórkowe|
|**Dystrybucja przez Internet**|Nie można łatwo rozpowszechniać przez Internet ze względu na ogromny rozmiar pliku |Kompaktowy rozmiar pliku ułatwia dystrybucję przez Internet|
|**Zgodność**|Najpopularniejszy kodek do słuchania muzyki i dźwięku, który jest prawie kompatybilny z każdym urządzeniem na świecie.Zgodny z komputerami nowej generacji, telefonami, amplitunerami AV, odtwarzaczami Blu-ray, urządzeniami do przesyłania strumieniowego, takimi jak Roku lub Fire TV|

## Bibliografia ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

