---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP-tiedostolomakeat
linktitle: STEP
description: Lansaitse STEP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata STEP-tiedostons.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Mikä on STEP-tiedosto?

STEP-tiedosto on laajalti käytetty tiedonvaihtomuoto tietokoneavusteiseen suunnitteluun (CAD). ISO-komitea standardoi sen vuonna 1994 nimellä ISO 10303-21. ISO 10303-21 määrittelee koodausmekanismin tietojen esittämiseksi EXPRESS-tietomallinnuskielellä. STEP-tiedosto tunnetaan myös nimellä p21-File ja STEP Physical File. STEP-tiedoston tiedostotunnisteet ovat .stp ja .step.

## Perushistoria

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. Toinen painos julkaistiin vuonna 2002, ja se sisälsi useiden tietoosien oikaisun ja laajennukset. Kolmas painos julkaistiin vuonna 2016, ja siihen lisättiin ankkuri- ja viiteosat, jotka sallivat entiteettien ja arvojen tallentamisen ulkoisiin tiedostoihin. UTF-8-tuki lisättiin merkkijonoihin. Digitaaliset allekirjoitukset lisättiin tiedoston sisällön tarkistamiseksi ja valtuustietojen vahvistamiseksi. Lisättiin myös tuki vaihtorakenteen pakkaamiseen ja tallentamiseen ZIP:n avulla.

## STEP-tiedostomuoto

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; ovat ensimmäisen tietueen ensimmäiset merkit. Kommentit on ympäröity /*- ja */-merkeillä. Viimeinen tietue sisältää END-ISO-10303-21; jos STEP-tiedosto on vuoden 2002 version mukainen. Jos se on vuoden 2016 version mukainen, END-ISO-10303-21;:n jälkeen voi olla yksi tai useampi digitaalinen allekirjoitus. terminaattori. Rivinvaihdot on merkitty \N\ ja sivunvaihdot on merkitty \F\.

STEP-tiedosto on jaettu osiin ja niiden nimet ovat varattuja termejä. Kaikki osiot päättyvät ENDSEC-tietueeseen, ja niiden on oltava alla näytetyssä järjestyksessä.

- **HEADER**: Tämä on pakollinen osio, jota ei voi toistaa. Se koostuu seuraavista kokonaisuuksista:
  - file_description (mandatory)
  - "tiedoston_nimi (pakollinen)"
  - "file_schema (pakollinen)"
  - "schema_population (valinnainen)"
  - "file_population (valinnainen)"
  - "section_language (valinnainen)"
  - "section_context (valinnainen)"
- **ANKKURI**: Se on valinnainen ei-toistuva osa, joka otettiin käyttöön vuoden 2016 versiossa. Se määrittää ilmentymien ulkoiset nimet, jotta niihin voidaan viitata.
- **VIITE**: Se on valinnainen ei-toistuva osa, joka otettiin käyttöön myös vuoden 2016 versiossa. Jokainen tämän osan merkintä liittää merkinnän/arvon ilmentymän nimen ulkoisen tiedoston ilmentymään/arvoon.
- **DATA**: Se on valinnainen toistettavissa oleva osa, joka sisältää malliinstanssin ydinsisällön.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## Viitteet

- {{HYPERLINKKI1}}

