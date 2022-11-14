---
date: 2019-12-09
keywords: arj, .arj, arj-bestandsindeling, hoe arj-bestanden te openen, .arj-extensie, arj-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ-bestandsindeling
linktitle: ARJ
description: "Meer informatie over ARJ-bestandsindelingen en API's die ARJ-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Wat is een ARJ-bestand? ##

ARJ (gearchiveerd door Robert Jung) is een zeer efficiënt gecomprimeerd archiefbestand ontwikkeld door Robert K. Jung. ARJ is begin jaren negentig ontwikkeld voor DOS en vroege versies van Windows. ARJ-bestanden zijn handig voor het maken van back-ups of het delen van een groot aantal bestanden, omdat u niet al die bestanden hoeft bij te houden en er maar één bestand is om te verwerken. De .arj-extensie wordt gebruikt voor de ARJ-archiefbestanden.

## ARJ-bestandsindeling ##

Een ARJ-bestand bevat twee soorten headers:

- Hoofdkop: Er is één hoofdkop aan het begin van het archief.
- Lokale headers: Lokale headers zijn aanwezig voor elk bestand.

|Offset|Type|Tellen|Beschrijving|
|---|---|---|---|
|0000h|woord|1|ID=0EA60h|
|0002h|woord|1|basis kopgrootte|
|0004h|byte|1|Grootte van kop|
|0005h|byte|1|Archiver versienummer|
|0006h|byte|1|Minimaal versienummer nodig|
|0007h|byte|1|Host-besturingssysteem:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Systeem xx)</br> 5 - OS/2</br> 6 - APPEL GS</br> 7 - ATARI ST</br> 8 - NeXT</br> 9 - VAX VMS|
|0008h|byte|1|Interne vlaggen, bitmap:</br> 0 - geen wachtwoord / wachtwoord</br> 1 - gereserveerd</br> 2 - bestand gaat verder op volgende schijf</br> 3 - veld startpositie bestand is beschikbaar</br> 4 - padvertaling ("\" naar "/" )|
|0009h|byte|1|Compressiemethode:</br> 0 - opgeslagen</br> 1 - meest gecomprimeerd</br> 2 - gecomprimeerd</br> 3 - sneller gecomprimeerd</br> 4 - snelste gecomprimeerd|
|000Ah|byte|1|Bestandstype:</br> 0 - binair</br> 1 - 7-bits tekst</br> 2 - commentaarkop</br> 3 - map</br> 4 - volumelabel|
|000Bh|byte|1|gereserveerd|
|000Ch|dword|1|Datum/tijd van origineel bestand in MS-DOS-formaat|
|0010h|dword|1|Grootte van het gecomprimeerde bestand|
|0014h|dword|1|Grootte van het originele bestand"|
|0018h|dword|1|CRC-32 van het originele bestand|
|001Ah|woord|1|Bestandsspecificatie in bestandsnaam|
|001Ch|woord|1|Bestandskenmerken|
|001Eh|woord|1|Hostgegevens|
|?|dword|1|Uitgebreide startpositie van bestand|
|????h|dword|1|CRC-32 van de basisheader|
|????h|word|1|Grootte van de eerste uitgebreide kop|
|????h+"SIZ"+2|dword|1|CRC-32 van de uitgebreide header|
|????h+"SIZ"+6|byte|?|Gecomprimeerd bestand|

## Referenties ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

