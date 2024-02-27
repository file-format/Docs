---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML fil formularat
linktitle: TOML
description: Ltjene om TOML filformat og API'er, der kan oprette og åbne TOML fils.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Hvad er TOML fil? ##

TOML (Tom's Obvious Minimal Language) er et minimalt konfigurationsfilformat, der bruger filtypenavnet .toml. TOML sigter efter at være let at læse, at kortlægge entydigt til ordbøger og at være let at parse til forskellige datastrukturer. TOML har en open source-specifikation, der modtog bidrag fra fællesskabet. TOML understøttes af mange programmeringssprog som C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift osv. MIME-typen for TOML-filer er *application/toml*.


## TOML filformat ##

TOML-filer består hovedsageligt af nøgle/værdi-par, sektioner/tabeller, kommentarer og skal være et gyldigt UTF-8-kodet Unicode-dokument. TOML understøtter datatyperne String, Integer, Float, Boolean, Datetime, Array og Table (hash-tabel/ordbog). TOML er et sprog, der skelner mellem store og små bogstaver.

### Syntaks ###

- **Nøgle-værdi-par**: Nøgle-værdi-par adskilles med lighedstegn (=). Hvert par skal være på en ny linje.

``` toml
første = Tom
sidste = Preston-Werner
```

- **Kommentarer**: Kommentarer begynder med hash-symbolet (#).

``` toml
# Dette er et TOML-dokument.
```

- **Strings**: Strenge er omgivet af anførselstegn ().

``` toml
string = Eksempel streng
```

- **Flerlinjestrenge**: Flerlinjede strenge er omgivet af tre anførselstegn ().

``` toml
[hjemme adresse]
street = 123 Tornado Alley
Suite 16
by = East Centerville
tilstand = KS
```

- **heltal/flydende**

``` toml
heltal = 20
flyder = 20,5
```

- **Booleaner**: Booleaner er altid små bogstaver.

``` toml
bool1 = sand
bool2 = falsk
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

``` toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
local_date = 1979-05-27
lokal_tid = 07:32:00
```

- **Arrays**: Arrays er omgivet af firkantede parenteser med elementer adskilt af kommaer (,).

``` toml
farver = [ rød, gul, grøn ]
```

- **Tabeller**: Tabeller er samlinger af nøgle/værdi-par, der er defineret af overskrifter på en ny linje omgivet af firkantede parenteser ([]). Tabellen slutter, når en ny header er angivet, eller når filen slutter.

``` toml
[hjemme adresse]
street = 123 Tornado Alley
Suite 16
by = East Centerville
tilstand = KS

[kontoradresse]
street = 123 Tornado Alley
Suite 16
by = East Centerville
tilstand = KS
```

Indlejrede tabeller er omgivet af krøllede klammer ({}) med hvert nøgle/værdi-par adskilt af komma (,).

``` toml
name = { first = Tom, last = Pitt }
```

## Referencer ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

