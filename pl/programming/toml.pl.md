---
date: 2019-10-11
keywords: toml, .toml, format pliku toml, jak otwierać pliki toml, rozszerzenie .toml, rozszerzenie toml
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku TOML
linktitle: TOML
description: "Dowiedz się więcej o formacie plików TOML i interfejsach API, które umożliwiają tworzenie i otwieranie plików TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Czym jest plik TOML? ##

TOML (Tom's Obvious Minimal Language) to minimalny format pliku konfiguracyjnego, który używa rozszerzenia .toml. TOML ma być łatwy do odczytania, jednoznacznie odwzorowywany na słowniki i łatwy do analizowania różnych struktur danych. TOML ma specyfikację open source, która otrzymała wkład społeczności. TOML jest obsługiwany przez wiele języków programowania, takich jak C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift itp. Typ MIME dla plików TOML to *application/toml*.


## Format pliku TOML ##

Pliki TOML składają się głównie z par klucz/wartość, sekcji/tabel, komentarzy i muszą być prawidłowym dokumentem Unicode zakodowanym w UTF-8. TOML obsługuje typy danych String, Integer, Float, Boolean, Datetime, Array i Table(hash table/dictionary). TOML jest językiem rozróżniającym wielkość liter.

### Składnia ###

- **Pary klucz-wartość**: pary klucz-wartość są oddzielone znakiem równości (=). Każda para musi znajdować się w nowej linii.

```toml
pierwszy = „Tomek”
last = „Preston-Werner”
```

- **Komentarze**: komentarze zaczynają się od symbolu krzyżyka (#).

```toml
# To jest dokument TOML.
```

- **Stringi**: Ciągi są ujęte w cudzysłowy (").

```toml
ciąg = "Przykładowy ciąg"
```

- **Ciągi wielowierszowe**: Ciągi wielowierszowe są ujęte w trzy cudzysłowy (""").

```toml
[adres domowy]
street = """Aleja Tornado 123
Apartament 16"""
miasto = „Wschodnie centrum miasta”
stan = "KS"
```

- **Liczby całkowite/liczby zmiennoprzecinkowe**

```toml
liczba całkowita = 20
liczba zmiennoprzecinkowa = 20,5
```

- **Booleany**: Booleany są zawsze pisane małymi literami.

```toml
bool1 = prawda
bool2 = fałsz
```

- **Data-godzina**: w przypadku daty i godziny można użyć daty i godziny w formacie RFC 3339, jak pokazano w poniższym przykładzie.

```toml
offset_date_time = 1979-05-27 07:32:00Z
lokalna_data_czas = 1979-05-27T07:32:00
lokalna_data = 1979-05-27
czas_lokalny = 07:32:00
```

- **Tablice**: Tablice są ujęte w nawiasy kwadratowe z elementami oddzielonymi przecinkami (,).

```toml
kolory = [ "czerwony", "żółty", "zielony" ]
```

- **Tabele**: tabele to kolekcje par klucz/wartość, które są zdefiniowane przez nagłówki w nowym wierszu otoczone nawiasami kwadratowymi ([]). Tabela kończy się po podaniu nowego nagłówka lub po zakończeniu pliku.

```toml
[adres domowy]
street = """Aleja Tornado 123
Apartament 16"""
miasto = „Wschodnie centrum miasta”
stan = "KS"

[adres biura]
street = """Aleja Tornado 123
Apartament 16"""
miasto = „Wschodnie centrum miasta”
stan = "KS"
```

Tabele wbudowane są otoczone nawiasami klamrowymi ({}), a każda para klucz/wartość jest oddzielona przecinkiem (,).

```toml
imię = { pierwsze = "Tomek", ostatnie = "Pitt" }
```

## Bibliografia ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

