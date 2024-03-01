---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: Ltienaa SPC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SPC-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Mikä on SPC-tiedosto?

Tiedosto, jonka pääte on .spc, on digitaalinen suojaussertifikaattitiedosto, joka on luotu PKCS # 7 -muodossa. Useat sovellukset luovat nämä varmennetiedostot turvallista tiedonvaihtoa varten. Harvoja tällaisia sovelluksia ovat OpenSSL ja Microsoftin .NET Frameworkiin sisältyvä Signcode.exe-sovellus. Kuten muutkin varmennetiedostot, kuten [.cer](/web/cer/), [.p7c](/web/p7c/) ja [.ssp](/web/ssp/), SPC-tiedostot sisältävät julkisen avaimen tiedot, jotka on salattu yksityisellä avaimella. Tämä julkinen avain voidaan jakaa käyttäjien kanssa julkisesti samalla, kun yksityinen avain pidetään luottamuksellisina.

## SPC-tiedostomuoto - lisätietoja

SPC-tiedostot tallennetaan levylle binääritiedostoina, jotka voidaan avata millä tahansa tekstieditorilla, mutta jotka eivät ole ihmisen luettavissa. Nämä perustuvat PKCS # 7:n uusimpaan versioon, joka on saatavilla {{HYPERLINKKI}}.

## Viitteet

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [SSP-viite](https://scalate.github.io/scalate/documentation/ssp-reference.html)


