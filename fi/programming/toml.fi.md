---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML-tiedostolomakeat
linktitle: TOML
description: Lansaita TOML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TOML-tiedostons.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Mikä on TOML-tiedosto? ##

TOML (Tom's Obvious Minimal Language) on pienimuotoinen määritystiedostomuoto, joka käyttää .toml-tunnistetta. TOML pyrkii olemaan helppolukuinen, kartoittaa yksiselitteisesti sanakirjoihin ja olla helposti jäsennettävä erilaisiin tietorakenteisiin. TOML:llä on avoimen lähdekoodin määritys, joka on saanut yhteisön lahjoituksia. TOML:ää tukevat monet ohjelmointikielet, kuten C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift jne. TOML-tiedostojen MIME-tyyppi on *application/toml*.


## TOML-tiedostomuoto ##

TOML-tiedostot koostuvat pääasiassa avain/arvo-pareista, osioista/taulukoista, kommenteista ja niiden on oltava kelvollinen UTF-8-koodattu Unicode-asiakirja. TOML tukee String-, Integer-, Float-, Boolean-, Datetime-, Array- ja Table (hash-taulukko/sanakirja) -tietotyyppejä. TOML on isot ja pienet kirjaimet erotteleva kieli.

### Syntaksi ###

- **Avain-arvoparit**: Avainarvoparit erotetaan yhtäläisyysmerkillä (=). Jokaisen parin on oltava uudella rivillä.

``` toml
ensimmäinen = Tom
viimeinen = Preston-Werner
```

- **Kommentit**: Kommentit alkavat hash-symbolilla (#).

``` toml
# Tämä on TOML-asiakirja.
```

- **Jotut**: Merkkijonot on ympäröity lainausmerkeillä ().

``` toml
string = Esimerkkijono
```

- **Moniriviset merkkijonot**: Moniriviset merkkijonot on ympäröity kolmella lainausmerkillä ().

``` toml
[kotiosoite]
street = 123 Tornado Alley
Sviitti 16
kaupunki = East Centerville
tila = KS
```

- **Kokonaisluvut/kellukkeet**

``` toml
kokonaisluku = 20
kelluva = 20,5
```

- **Totuusarvot**: Boolen arvot ovat aina pieniä kirjaimia.

``` toml
bool1 = tosi
bool2 = false
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

``` toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
paikallinen_päivämäärä = 27.5.1979
paikallinen_aika = 07:32:00
```

- **Matriisit**: Taulukot on ympäröity hakasulkeilla, joiden elementit on erotettu pilkuilla (,).

``` toml
värit = [ punainen, keltainen, vihreä ]
```

- **Taulukot**: Taulukot ovat avain/arvo-parien kokoelmia, jotka määritellään otsikoilla uudella rivillä, jota ympäröivät hakasulkeet ([]). Taulukko päättyy, kun uusi otsikko annetaan tai kun tiedosto päättyy.

``` toml
[kotiosoite]
street = 123 Tornado Alley
Sviitti 16
kaupunki = East Centerville
tila = KS

[toimisto-osoite]
street = 123 Tornado Alley
Sviitti 16
kaupunki = East Centerville
tila = KS
```

Sisäiset taulukot on ympäröity aaltosulkeilla ({}), ja kukin avain/arvo-pari on erotettu pilkulla (,).

``` toml
nimi = { ensimmäinen = Tom, viimeinen = Pitt }
```

## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

