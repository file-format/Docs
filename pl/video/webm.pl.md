---
date: 2019-10-11
keywords: WEBM, Co to jest plik WEBM, Format pliku WEBM
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików WEBM i interfejsach API, które mogą tworzyć i otwierać pliki WEBM."
title: WEBM — format pliku wideo WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Czym jest plik WEBM?

Plik z rozszerzeniem .webm to plik wideo oparty na otwartym, nieodpłatnym formacie pliku WebM. Został zaprojektowany do udostępniania wideo w Internecie i definiuje strukturę kontenera plików, w tym formaty wideo i audio. WebM jest w 100% darmowy, implementuje wysokiej jakości rozwiązania oparte na otwartych technologiach, takich jak HTML, HTTP i TCP/IP, które są otwarte dla każdego. WebM został specjalnie zaprojektowany do obsługi wideo w Internecie, dzięki czemu jest zoptymalizowany do przesyłania strumieniowego przy niskim zużyciu mocy obliczeniowej. Dzięki temu nadaje się do odtwarzania filmów na dowolnym urządzeniu, zwłaszcza na netbookach o niskim poborze mocy, komputerach przenośnych i tabletach.

## Format pliku WEBM

Struktura plików WebM jest oparta na podzbiorze formatu pliku kontenera Matroska [MKV](/pl/video/mkv/). Strumienie wideo dostępne w pliku WebM są kompresowane przy użyciu technologii kompresji VP8 lub VP9, które są bardzo wydajne w kompresji. Podobnie strumienie audio w pliku WebM są kompresowane przy użyciu kodeków Vorbis lub Opus opracowanych przez [Xiph Foundation](https://www.xiph.org/). Wszystkie te kodeki wideo i audio są bezpłatne i można z nich korzystać bez żadnych opłat.

Poniżej przedstawiono podsumowanie specyfikacji formatu pliku WebM.

|Pole|Opis|
---|---|
|Typ MIME |wideo/webm|
|Tylko audio typu MIME |audio/webm|
|Jednolity Identyfikator Typu| org.webmprojekt.webm|
|Nazwa kodeka wideo| VP8 lub VP9|
|Nazwa kodeka audio| Vorbis lub Opus|

### Elementy WebM

WebM, będący podzbiorem specyfikacji Matroski, zapewnia wsparcie dla niektórych funkcjonalności Matroski. Poniżej znajduje się opis obsługiwanych elementów.

#### EBML

|Nazwa |Opis|
---|---|
|EBML|Ustaw charakterystykę EBML danych do naśladowania. Każdy dokument EBML musi zaczynać się od tego.|
|EBMLVersion |Wersja parsera EBML użytego do utworzenia pliku.|
|EBMLReadVersion|Minimalna wersja EBML, którą parser musi obsługiwać, aby odczytać ten plik.|
|EBMLMaxIDLength |Maksymalna długość identyfikatorów, które znajdziesz w tym pliku (4 lub mniej w Matrosce).|
|EBMLMaxSizeLength|Maksymalna długość rozmiarów, które znajdziesz w tym pliku (8 lub mniej w Matrosce). Nie zastępuje to rozmiaru elementu wskazanego na początku elementu. Elementy, które mają wskazany rozmiar większy niż dozwolony przez EBMLMaxSizeLength, zostaną uznane za nieważne.|
|DocType|Ciąg opisujący typ dokumentu następujący po tym nagłówku EBML (w naszym przypadku „webm”).|
|DocTypeVersion|Wersja interpretera DocType użytego do utworzenia pliku.|
|DocTypeReadVersion|Minimalna wersja DocType, którą interpreter musi obsługiwać, aby odczytać ten plik.|

#### Elementy globalne

W tej chwili obsługiwany jest tylko element „Void”, który służy do unieważniania uszkodzonych danych, aby uniknąć nieoczekiwanych zachowań podczas korzystania z uszkodzonych danych. Treść jest odrzucana. Służy również do rezerwowania miejsca w elemencie podrzędnym do późniejszego wykorzystania.

#### Człon
Ten element zawiera wszystkie inne elementy najwyższego poziomu (poziom 1). Zazwyczaj plik Matroska składa się z 1 segmentu.

#### Meta Szukaj informacji

Obsługiwane jest wyszukiwanie następujących informacji.

|Nazwa elementu |Opis|
---|---|
|SeekHead |Zawiera pozycję innego elementu poziomu 1.|
|Seek |Zawiera pojedynczy wpis wyszukiwania elementu EBML.|
|SeekID |Identyfikator binarny odpowiadający nazwie elementu.|
|SeekPosition |Pozycja elementu w segmencie w oktetach (0 = element pierwszego poziomu 1).|

## Bibliografia

* [WebM](https://www.webmproject.org/)
* [Repozytoria kodu WebM](https://www.webmproject.org/code/#webp-repositories)

