---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD-tiedostomuoto - Python Dynamic Module
linktitle: PYD
description: Ltienaa PYD-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata PYD-tiedostons.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Mikä on PYD-tiedosto?

PYD-tiedosto on Pythonilla kirjoitettu dynaaminen linkkikirjasto, joka voidaan suorittaa muulla Python-koodilla ajon aikana. Se sisältää yhden tai useamman Python-moduulin, joka helpottaa koodin uudelleenkäyttöä ja tarjoaa moduuliarkkitehtuurin sovellusten kirjoittamista varten. PYD-tiedostoja voidaan luoda ja tallentaa .pyd-tunnisteella, esim. helloworld.pyd. Sovelluskehittäjät voivat sisällyttää PYD-moduulit sovelluksiinsa tuontilausekkeen avulla. PYD-tiedostot voidaan avata Python Software Foundation Pythonilla, joka on saatavilla Windows-, Mac- ja Linux-käyttöjärjestelmille.

## PYD-tiedostomuoto - lisätietoja

PYD-tiedostot on kirjoitettu Python-ohjelmointikielellä ja ne luodaan kääntämällä Python-koodia.

## Ero PY- ja PYD-tiedostomuotojen välillä

[PY](/programming/py/)-tiedosto sisältää lähdekoodia, joka suoritetaan sellaisenaan, eikä sitä voida sisällyttää uudelleen käytettävänä koodina muihin Python-sovelluksiin. PYD-tiedosto on kuitenkin dynaamisesti linkitetty kirjasto, jota käytetään Windows-käyttöjärjestelmässä.

## Kuinka luodaan PYD-tiedosto?

PYD-tiedosto voidaan luoda luomalla moduuli, jonka nimi on esim. exmaple.pyd. Tämä moduuli sisältää kaikki toiminnot yhden tai useamman funktion muodossa, esim. PyMod_example(). Kun ohjelma sisältää tämän kirjaston ja kutsuu sitä, se voidaan tehdä tuomalla moduuli ja funktio PyMod_example() suoritetaan.

## Viitteet ##

 * [Python-laajennusten luominen C/C++:ssa](https://sebsauvage.net/python/mingw.html)
 * [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))
