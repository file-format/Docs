---
date: 2019-10-11
keywords: toml, .toml, toml-filformat, hur man öppnar toml-filer, .toml-tillägg, toml-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML filformat
linktitle: TOML
description: "Lär dig om TOML-filformat och API:er som kan skapa och öppna TOML-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Vad är TOML fil? ##

TOML (Tom's Obvious Minimal Language) är ett minimalt konfigurationsfilformat som använder tillägget .toml. TOML syftar till att vara lätt att läsa, att entydigt mappa till ordböcker och att vara lätt att tolka till olika datastrukturer. TOML har en öppen källkodsspecifikation som fick bidrag från samhället. TOML stöds av många programmeringsspråk som C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. MIME-typen för TOML-filer är *application/toml*.


## TOML-filformat ##

TOML-filer består huvudsakligen av nyckel/värdepar, sektioner/tabeller, kommentarer och måste vara ett giltigt UTF-8-kodat Unicode-dokument. TOML stöder datatyperna String, Integer, Float, Boolean, Datetime, Array och Table (hash-tabell/ordbok). TOML är ett skiftlägeskänsligt språk.

### Syntax ###

- **Nyckel-värde-par**: Nyckel-värde-par separeras med likhetstecken (=). Varje par måste vara på en ny linje.

``` toml
första = "Tom"
sista = "Preston-Werner"
```

- **Kommentarer**: Kommentarer börjar med hash-symbolen (#).

``` toml
# Detta är ett TOML-dokument.
```

- **Strängar**: Strängar är omgivna av citattecken (").

``` toml
string = "Exempelsträng"
```

- **Flerradiga strängar**: Flerradiga strängar omges av tre citattecken (""").

``` toml
[hemadress]
gata = """123 Tornado Alley
Svit 16"""
stad = "East Centerville"
tillstånd = "KS"
```

- **Heltal/Flytande**

``` toml
heltal = 20
flyta = 20,5
```

- **Booleans**: Booleans är alltid gemener.

``` toml
bool1 = sant
bool2 = falskt
```

- **Date-Time**: För DateTime kan du använda en RFC 3339-formaterad datum-tid som visas i exemplet nedan.

``` toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
local_date = 1979-05-27
lokal_tid = 07:32:00
```

- **Arrayer**: Arrayer är omgivna av hakparenteser med element separerade med kommatecken (,).

``` toml
färger = [ "röd", "gul", "grön" ]
```

- **Tabell**: Tabeller är samlingar av nyckel/värdepar som definieras av rubriker på en ny linje omgiven av hakparenteser ([]). Tabellen slutar när en ny rubrik tillhandahålls eller när filen slutar.

``` toml
[hemadress]
gata = """123 Tornado Alley
Svit 16"""
stad = "East Centerville"
tillstånd = "KS"

[kontorsadress]
gata = """123 Tornado Alley
Svit 16"""
stad = "East Centerville"
tillstånd = "KS"
```

Inline-tabeller omges av klammerparenteser ({}) med varje nyckel/värdepar separerade med kommatecken (,).

``` toml
namn = { första = "Tom", sista = "Pitt" }
```

## Referenser ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

