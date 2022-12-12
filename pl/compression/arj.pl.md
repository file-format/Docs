---
date: 2019-12-09
keywords: arj, .arj, format pliku arj, jak otwierać pliki arj, rozszerzenie .arj, rozszerzenie arj
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku ARJ
linktitle: ARJ
description: "Dowiedz się więcej o formacie plików ARJ i interfejsach API, które mogą tworzyć i otwierać pliki ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Czym jest plik ARJ? ##

ARJ (zarchiwizowane przez Roberta Junga) to skompresowany plik archiwum o wysokiej wydajności opracowany przez Roberta K. Junga. ARJ został opracowany dla systemu DOS i wczesnych wersji systemu Windows na początku lat 90. Pliki ARJ są przydatne do tworzenia kopii zapasowych lub udostępniania dużej liczby plików, ponieważ nie trzeba śledzić wszystkich tych plików, a do obsługi jest tylko jeden plik. Rozszerzenie .arj jest używane dla plików archiwum ARJ.

## Format pliku ARJ ##

Plik ARJ zawiera dwa typy nagłówków:

- Główny nagłówek: Na początku archiwum znajduje się jeden główny nagłówek.
- Lokalne nagłówki: Lokalne nagłówki są obecne przed każdym plikiem.

|Przesunięcie|Typ|Liczba|Opis|
|---|---|---|---|
|0000h|słowo|1|ID=0EA60h|
|0002h|słowo|1|podstawowy rozmiar nagłówka|
|0004h|bajt|1|Rozmiar nagłówka|
|0005h|bajt|1|Numer wersji archiwizatora|
|0006h|bajt|1|Minimalny wymagany numer wersji|
|0007h|bajt|1|System operacyjny hosta:</br> 0 — MS-DOS</br> 1 - PIERWOTNE</br> 2 — UNIX</br> 3 - AMIGA</br> 4 — MAC-OS (system xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ul</br> 8 - Dalej</br> 9 - VAX VMS|
|0008h|bajt|1|Flagi wewnętrzne, bitmapowe:</br> 0 - brak hasła / hasła</br> 1 - zarezerwowane</br> 2 - plik jest kontynuowany na następnym dysku</br> 3 - dostępne jest pole pozycji początkowej pliku</br> 4 - tłumaczenie ścieżki ( "\" na "/" )|
|0009h|bajt|1|Metoda kompresji:</br> 0 - zapisane</br> 1 - najbardziej skompresowany</br> 2 - skompresowany</br> 3 - skompresowany szybciej</br> 4 - skompresowany najszybciej|
|000Ah|bajt|1|Typ pliku:</br> 0 - binarny</br> 1 - 7-bitowy tekst</br> 2 - nagłówek komentarza</br> 3 - katalog</br> 4 - etykieta woluminu|
|000Bh|bajt|1|zarezerwowany|
|000Ch|dword|1|Data/czas oryginalnego pliku w formacie MS-DOS|
|0010h|dword|1|Rozmiar skompresowanego pliku|
|0014h|dword|1|Rozmiar oryginalnego pliku"|
|0018h|dword|1|CRC-32 oryginalnego pliku|
|001Ah|słowo|1|Pozycja specyfikacji pliku w nazwie pliku|
|001Ch|słowo|1|Atrybuty pliku|
|001Eh|słowo|1|Dane hosta|
|?|dword|1|Pozycja początkowa rozszerzonego pliku|
|????h|dword|1|CRC-32 podstawowego nagłówka|
|????h|słowo|1|Rozmiar pierwszego rozszerzonego nagłówka|
|????h+"SIZ"+2|dword|1|CRC-32 rozszerzonego nagłówka|
|????h+"SIZ"+6|bajt|?|Plik skompresowany|

## Bibliografia ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

