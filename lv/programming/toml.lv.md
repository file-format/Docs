---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML faila veidlapaat
linktitle: TOML
description: Lnopelniet par TOML faila formātu un API, kas var izveidot un atvērt TOML failus.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Kas ir TOML fails? ##

TOML (Toma acīmredzamā minimālā valoda) ir minimālās konfigurācijas faila formāts, kurā tiek izmantots paplašinājums .toml. TOML mērķis ir viegli lasāms, nepārprotami kartējams vārdnīcās un viegli parsējams dažādās datu struktūrās. TOML ir atvērtā koda specifikācija, kas saņēma kopienas ieguldījumu. TOML atbalsta daudzas programmēšanas valodas, piemēram, C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift utt. TOML failu MIME tips ir *application/toml*.


## TOML faila formāts ##

TOML faili galvenokārt sastāv no atslēgu/vērtību pāriem, sadaļām/tabulām, komentāriem, un tiem jābūt derīgam UTF-8 kodētam unikoda dokumentam. TOML atbalsta datu tipus String, Integer, Float, Boolean, Datetime, Array un Table (jaucēj tabula/vārdnīca). TOML ir reģistrjutīga valoda.

### Sintakse ###

- **Atslēgas-vērtību pāri**: atslēgu un vērtību pāri ir atdalīti ar vienādības zīmi (=). Katram pārim jāatrodas jaunā rindā.

``` toml
pirmais = Toms
pēdējais = Prestons-Verners
```

- **Komentāri**: komentāri sākas ar jaucējzīmi (#).

``` toml
# Šis ir TOML dokuments.
```

- **Stīgas**: virknes ieskauj pēdiņās ().

``` toml
string = Piemēra virkne
```

- **Vairāku rindu virknes**: vairāku rindu virknes ieskauj trīs pēdiņās ().

``` toml
[mājas adrese]
iela = 123 Tornado aleja
Suite numurs 16
pilsēta = Austrumcentrvila
stāvoklis = KS
```

- **Veseli skaitļi/peldošie skaitļi**

``` toml
vesels skaitlis = 20
pludiņš = 20,5
```

- ** Būla vērtības**: Būla vērtības vienmēr ir mazie burti.

``` toml
bool1 = patiess
bool2 = false
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

``` toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
vietējais_datums = 1979.05.27
vietējais_laiks = 07:32:00
```

- **Masīvi**: masīvus ieskauj kvadrātiekavas ar elementiem, kas atdalīti ar komatiem (,).

``` toml
krāsas = [ sarkans, dzeltens, zaļš]
```

- **Tabulas**: tabulas ir atslēgu/vērtību pāru kolekcijas, kas ir noteiktas ar galvenēm jaunā rindā, ko ieskauj kvadrātiekavas ([]). Tabula beidzas, kad tiek nodrošināta jauna galvene vai fails beidzas.

``` toml
[mājas adrese]
iela = 123 Tornado aleja
Suite numurs 16
pilsēta = Austrumcentrvila
stāvoklis = KS

[biroja adrese]
iela = 123 Tornado aleja
Suite numurs 16
pilsēta = Austrumcentrvila
stāvoklis = KS
```

Iekļautās tabulas ieskauj cirtaini iekavas ({}), katrs atslēgas/vērtības pāris ir atdalīts ar komatu (,).

``` toml
vārds = { pirmais = Toms, pēdējais = Pits}
```

## Atsauces Nr.

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

