---
date: 2019-10-11
keywords: toml, .toml, toml-bestandsindeling, hoe toml-bestanden te openen, .toml-extensie, toml-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML-bestandsindeling
linktitle: TOML
description: "Meer informatie over TOML-bestandsindelingen en API's die TOML-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Wat is een TOML-bestand? ##

TOML (Tom's Obvious Minimal Language) is een minimale configuratiebestandsindeling die de .toml-extensie gebruikt. TOML streeft ernaar gemakkelijk te lezen te zijn, ondubbelzinnig te koppelen aan woordenboeken en gemakkelijk te ontleden naar verschillende datastructuren. TOML heeft een open source-specificatie die communitybijdragen heeft ontvangen. TOML wordt ondersteund door vele programmeertalen zoals C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. Het MIME-type voor TOML-bestanden is *application/toml*.


## TOML-bestandsindeling ##

TOML-bestanden bestaan voornamelijk uit sleutel/waarde-paren, secties/tabellen, opmerkingen en moeten een geldig UTF-8-gecodeerd Unicode-document zijn. TOML ondersteunt gegevenstypen String, Integer, Float, Boolean, Datetime, Array en Table (hashtabel/woordenboek). TOML is een hoofdlettergevoelige taal.

### Syntaxis ###

- **Sleutel-waardeparen**: Sleutel-waardeparen worden gescheiden door een gelijkteken (=). Elk paar moet op een nieuwe regel staan.

``` toml
eerste = "Tom"
last = "Preston-Werner"
```

- **Opmerkingen**: opmerkingen beginnen met het hekje (#) symbool.

``` toml
# Dit is een TOML-document.
```

- **Strings**: Strings worden omgeven door aanhalingstekens ("").

``` toml
string = "Voorbeeld string"
```

- **Tekenreeksen met meerdere regels**: Tekenreeksen met meerdere regels worden omgeven door drie aanhalingstekens (""").

``` toml
[thuisadres]
straat = """123 Tornado Alley
Suite 16"""
city = "Oost Centreville"
staat = "KS"
```

- **Gehele getallen/floats**

``` toml
geheel getal = 20
vlotter = 20.5
```

- **Booleans**: Booleans zijn altijd kleine letters.

``` toml
bool1 = waar
bool2 = false
```

- **Date-Time**: voor DateTime kunt u een RFC 3339-geformatteerde datum-tijd gebruiken, zoals weergegeven in het onderstaande voorbeeld.

``` toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
local_date = 1979-05-27
lokale_tijd = 07:32:00
```

- **Arrays**: Arrays worden omgeven door vierkante haken met elementen gescheiden door komma's (,).

``` toml
kleuren = [ "rood", "geel", "groen"]
```

- **Tabellen**: tabellen zijn verzamelingen sleutel/waarde-paren die worden gedefinieerd door kopteksten op een nieuwe regel omringd door vierkante haken ([]). De tabel eindigt wanneer een nieuwe header wordt verstrekt of wanneer het bestand eindigt.

``` toml
[thuisadres]
straat = """123 Tornado Alley
Suite 16"""
city = "Oost Centreville"
staat = "KS"

[Kantoor adres]
straat = """123 Tornado Alley
Suite 16"""
city = "Oost Centreville"
staat = "KS"
```

Inline-tabellen zijn omgeven door accolades ({}) waarbij elk sleutel/waarde-paar wordt gescheiden door een komma (,).

``` toml
naam = { eerste = "Tom", laatste = "Pitt" }
```

## Referenties ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

