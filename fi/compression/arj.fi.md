---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ-tiedostolomakeat
linktitle: ARJ
description: Lansaitse ARJ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ARJ-tiedostons.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Mikä on ARJ-tiedosto? ##

ARJ (arkistoitu Robert Jung) on tehokas pakattu arkistotiedosto, jonka on kehittänyt Robert K. Jung. ARJ kehitettiin DOS:lle ja Windowsin varhaisille versioille 1990-luvun alussa. ARJ-tiedostot ovat hyödyllisiä varmuuskopioinnissa tai suuren tiedostomäärän jakamisessa, koska sinun ei tarvitse seurata kaikkia näitä tiedostoja ja käsiteltävänä on vain yksi tiedosto. ARJ-arkistotiedostoissa käytetään .arj-tunnistetta.

## ARJ-tiedostomuoto ##

ARJ-tiedosto sisältää kahden tyyppisiä otsikoita:

- Pääotsikko: Arkiston alussa on yksi pääotsikko.
- Paikalliset otsikot: Paikalliset otsikot ovat ennen jokaista tiedostoa.

|Offset|Tyyppi|Laskuri|Kuvaus|
|---|---|---|---|
|0000h|sana|1|ID=0EA60h|
|0002h|sana|1|otsikon peruskoko|
|0004h|tavu|1|Ylätunnisteen koko|
|0005h|tavu|1|Arkistoinnin versionumero|
|0006h|tavu|1|Vaadittu vähimmäisversionumero|
|0007h|tavu|1|Isäntäkäyttöjärjestelmä:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (System xx)</br> 5 - OS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - SEURAAVA</br> 9 - VAX VMS|
|0008h|tavu|1|Sisäiset liput, bittikartta:</br> 0 - ei salasanaa / salasanaa</br> 1 - varattu</br> 2 - tiedosto jatkuu seuraavalla levyllä</br> 3 - tiedoston aloituspaikkakenttä on käytettävissä</br> 4 - polun käännös ( \ - / )|
|0009h|tavu|1|Pakkausmenetelmä:</br> 0 - tallennettu</br> 1 - puristettu eniten</br> 2 - puristettu</br> 3 - pakattu nopeammin</br> 4 - pakattu nopein|
|000Ah|tavu|1|Tiedostotyyppi:</br> 0 - binääri</br> 1-7-bittinen teksti</br> 2 - kommentin otsikko</br> 3 - hakemisto</br> 4 - levyn etiketti|
|000Bh|tavu|1|varattu|
|000Ch|dword|1|Alkuperäisen tiedoston päivämäärä/aika MS-DOS-muodossa|
|0010h|dword|1|Pakatun tiedoston koko|
|0014h|dword|1|Alkuperäisen tiedoston koko|
|0018h|dword|1|alkuperäisen tiedoston CRC-32|
|001Ah|word|1|Tiedostokohtainen sijainti tiedostonimessä|
|001Ch|word|1|Tiedostomääritteet|
|001Eh|word|1|Isäntätiedot|
|?|dword|1|Laajennettu tiedoston aloituspaikka|
|????h|dword|1|perusotsikon CRC-32|
|????h|word|1|Ensimmäisen laajennetun otsikon koko|
|????h+SIZ+2|dword|1|laajennetun otsikon CRC-32|
|????h+SIZ+6|tavu|?|Pakattu tiedosto|

## Viitteet ##

- {{HYPERLINKKI1}}

