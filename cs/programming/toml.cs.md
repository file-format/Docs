---
date: 2019-10-11
keywords: toml, .toml, formát souboru toml, jak otevřít soubory toml, přípona .toml, přípona toml
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru TOML
linktitle: TOML
description: "Přečtěte si o formátu souboru TOML a rozhraních API, která mohou vytvářet a otevírat soubory TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Co je soubor TOML? ##

TOML (Tom's Obvious Minimal Language) je formát minimálního konfiguračního souboru, který používá příponu .toml. TOML si klade za cíl být snadno čitelný, jednoznačně mapovat do slovníků a snadno analyzovat různé datové struktury. TOML má specifikaci open source, která obdržela příspěvky komunity. TOML je podporováno mnoha programovacími jazyky jako C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift atd. Typ MIME pro soubory TOML je *application/toml*.


## Formát souboru TOML ##

Soubory TOML se skládají hlavně z párů klíč/hodnota, oddílů/tabulek, komentářů a musí se jednat o platný dokument Unicode kódovaný UTF-8. TOML podporuje datové typy String, Integer, Float, Boolean, Datetime, Array a Table (hash table/dictionary). TOML je jazyk citlivý na velká a malá písmena.

### Syntaxe ###

- **Páry klíč–hodnota**: Páry klíč–hodnota jsou odděleny znaménkem rovná se (=). Každý pár musí být na novém řádku.

```toml
první = "Tom"
poslední = "Preston-Werner"
```

- **Komentáře**: Komentáře začínají symbolem hash (#).

```toml
# Toto je dokument TOML.
```

- **Řetězce**: Řetězce jsou ohraničeny uvozovkami (").

```toml
string = "Příkladový řetězec"
```

- **Víceřádkové řetězce**: Víceřádkové řetězce jsou obklopeny třemi uvozovkami (""").

```toml
[domovní adresa]
ulice = """123 Tornádo Alley
Suite 16"""
město = "East Centerville"
stav = "KS"
```

- **Celá čísla/plovoucí čísla**

```toml
celé číslo = 20
plovoucí = 20,5
```

- **Booleans**: Logické hodnoty jsou vždy malá písmena.

```toml
bool1 = pravda
bool2 = false
```

- **Datum-čas**: Jako datum a čas můžete použít datum a čas ve formátu RFC 3339, jak je uvedeno v příkladu níže.

```toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
místní_datum = 1979-05-27
místní_čas = 07:32:00
```

- **Pole**: Pole jsou ohraničena hranatými závorkami s prvky oddělenými čárkami (,).

```toml
barvy = [ "červená", "žlutá", "zelená" ]
```

- **Tabulky**: Tabulky jsou kolekce párů klíč/hodnota, které jsou definovány záhlavím na novém řádku ohraničeném hranatými závorkami ([]). Tabulka končí, když je poskytnuto nové záhlaví nebo když končí soubor.

```toml
[domovní adresa]
ulice = """123 Tornádo Alley
Suite 16"""
město = "East Centerville"
stav = "KS"

[adresa kanceláře]
ulice = """123 Tornádo Alley
Suite 16"""
město = "East Centerville"
stav = "KS"
```

Vložené tabulky jsou ohraničeny složenými závorkami ({}), přičemž každý pár klíč/hodnota je oddělen čárkou (,).

```toml
jméno = { první = "Tom", poslední = "Pitt" }
```

## Reference ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

