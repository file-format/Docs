---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML failo formaat
linktitle: TOML
description: Luždirbti apie TOML failo formatą ir API, kurios gali sukurti ir atidaryti TOML failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Kas yra TOML failas? ##

TOML (Tom's Obvious Minimal Language) yra minimalus konfigūracijos failo formatas, kuriame naudojamas .toml plėtinys. TOML siekiama, kad jį būtų lengva skaityti, nedviprasmiškai susieti su žodynais ir kad būtų lengva analizuoti įvairias duomenų struktūras. TOML turi atvirojo kodo specifikaciją, kuri gavo bendruomenės indėlį. TOML palaiko daugelis programavimo kalbų, tokių kaip C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift ir kt. TOML failų MIME tipas yra *application/toml*.


## TOML failo formatas ##

TOML failus daugiausia sudaro raktų / reikšmių poros, skyriai / lentelės, komentarai ir turi būti galiojantis UTF-8 užkoduotas Unikodo dokumentas. TOML palaiko duomenų tipus String, Integer, Float, Boolean, Datetime, Array ir Table (maišos lentelė / žodynas). TOML yra didžiųjų ir mažųjų raidžių kalba.

### Sintaksė ###

- **Rakto-reikšmių poros**: rakto-reikšmių poros yra atskirtos lygybės ženklu (=). Kiekviena pora turi būti naujoje eilutėje.

``` toml
pirmas = Tomas
paskutinis = Prestonas-Verneris
```

- **Komentarai**: komentarai prasideda maišos (#) simboliu.

``` toml
# Tai TOML dokumentas.
```

- **Stygos**: eilutės pateikiamos kabutėse ().

``` toml
string = Eilutės pavyzdys
```

- **Kelių eilučių eilutės**: kelių eilučių eilutės yra apsuptos trimis kabutėmis ().

``` toml
[namų adresas]
gatvė = 123 Tornado alėja
Liukso numeris 16
miestas = East Centerville
būsena = KS
```

- **Sveikieji skaičiai / plūduriuojantys skaičiai**

``` toml
sveikas skaičius = 20
plūdė = 20,5
```

- **Booleans**: Būlios visada rašomos mažosiomis raidėmis.

``` toml
bool1 = tiesa
bool2 = klaidinga
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

``` toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
vietinė_data = 1979-05-27
vietinis_laikas = 07:32:00
```

- **Masyvai**: masyvai yra apsupti laužtiniais skliaustais su elementais, atskirtais kableliais (,).

``` toml
spalvos = [ raudona, geltona, žalia]
```

– **Lentelės**: lentelės yra raktų/reikšmių porų rinkiniai, apibrėžti antraštėmis naujoje eilutėje, apsuptoje laužtiniais skliaustais ([]). Lentelė baigiasi, kai pateikiama nauja antraštė arba kai baigiasi failas.

``` toml
[namų adresas]
gatvė = 123 Tornado alėja
Liukso numeris 16
miestas = East Centerville
būsena = KS

[biuro adresas]
gatvė = 123 Tornado alėja
Liukso numeris 16
miestas = East Centerville
būsena = KS
```

Eilutinės lentelės yra apsuptos riestiniais skliaustais ({}), o kiekviena rakto/reikšmių pora atskiriama kableliu (,).

``` toml
vardas = { pirmas = Tomas, paskutinis = Pitas }
```

## Nuorodos Nr.

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

