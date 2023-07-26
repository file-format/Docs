---
date: 2020-11-11
keywords: myi, .myi, format pliku myi, jak otwierać pliki myi, rozszerzenie .myi, rozszerzenie myi
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku MYI
linktitle: MYI
description: "Dowiedz się o formacie pliku MYI i interfejsach API, które mogą tworzyć i otwierać pliki MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Czym jest plik MYI? ##

MYI jest również znany jako plik indeksu MySQL MyISAM. Służy do przechowywania indeksów dla tabeli MyISAM przez MySQL. Indeks bazy danych MySQL określa strukturę tabeli i zawiera mechanizm kontroli sprawdzający integralność tabel.

## Format pliku MYI ##

Plik MYI składa się z dwóch części, nagłówka i wartości klucza.

### Nagłówek MYI ###

Nagłówek zawiera informacje o opcjach, rozmiarach plików i kluczach. Klucze w MySQL są tworzone za pomocą polecenia takiego jak

```sql
CREATE [UNIQUE] INDEX.
```

Pliki, które odczytują i zapisują pliki MYI, znajdują się w katalogu ./myisam. Posiada następujące pliki:

- mi_open.c: Ten plik zawiera procedury, które zapisują każdą sekcję nagłówka.
- mi_create.c: Ten plik zawiera procedury wywołujące procedury mi_open.c.
- myisamdef.h: Ten plik zawiera definicje struktur.

Nagłówek zawiera następujące sekcje:

- stan: stan jest zapisywany przez mi_open.c, mi_state_info_write(). Ta struktura występuje raz w pliku.
- base: Baza jest napisana przez mi_open.c, mi_base_info_write(). MI_BASE_INFO jest odpowiednią strukturą dla bazy w myisamdef.h. Ta struktura występuje raz w pliku.
- keydef: keydef jest zapisywany przez mi_open.c, mi_keydef_write(). MI_KEYDEF jest odpowiednią strukturą dla keydef w myisamdef.h. Jest to struktura wielu wystąpień, która pojawia się dla każdego indeksu.
- recinfo: Recinfo jest napisane przez mi_open.c, mi_recinfo_write(). MI_COLUMNDEF jest odpowiednią strukturą dla recinfo w myisamdef.h. Jest to struktura wielu wystąpień, która pojawia się raz dla każdego pola, które pojawia się w kluczu.

### Kluczowe wartości ###

Strony w MySQL nazywane są blokami. Kluczowe wartości są w blokach. Blok zawiera informacje tylko z jednego indeksu. Każdy klucz zawiera całą zawartość wszystkich kolumn. Normalna długość bloku to 0x0400 (1024) bajtów. Wskaźnik ma stały rozmiar (4 bajty) dla tabel o stałych wierszach, który zawiera porządkowy numer wiersza. Jeśli klucz jest pusty, to bajt to 0x00. Normalny blok jest wypełniony co najmniej w 65%, a zazwyczaj w 80%.

Plik myisamdef.h zawiera następujące informacje wyrażone w stałych. Maksymalna liczba kluczy to 32 (MI_MAX_KEY), a maksymalna liczba segmentów w kluczu to 16 (MI_MAX_KEY_SEG). Maksymalna długość klucza to 500 (MI_MAX_KEY_LENGTH). Maksymalna długość bloku to 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Bibliografia ##

- [Plik .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

