---
date: 2019-12-09
keywords: arj, .arj, format de fișier arj, cum se deschide fișierele arj, extensia .arj, extensia arj
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier ARJ
linktitle: ARJ
description: "Aflați despre formatul de fișier ARJ și despre API-urile care pot crea și deschide fișiere ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Ce este un fișier ARJ? ##

ARJ (Arhivat de Robert Jung) este un fișier de arhivă comprimat de înaltă eficiență dezvoltat de Robert K. Jung. ARJ a fost dezvoltat pentru DOS și versiunile timpurii de Windows la începutul anilor 1990. Fișierele ARJ sunt utile pentru a face backup sau a partaja un număr mare de fișiere, deoarece nu trebuie să țineți evidența tuturor acestor fișiere și există doar un singur fișier de gestionat. Extensia .arj este folosită pentru fișierele de arhivă ARJ.

## Format fișier ARJ ##

Un fișier ARJ conține două tipuri de anteturi:

- Antet principal: Există un antet principal la începutul arhivei.
- Anteturi locale: Antetele locale sunt prezente înaintea fiecărui fișier.

|Offset|Tip|Număr|Descriere|
|---|---|---|---|
|0000h|cuvânt|1|ID=0EA60h|
|0002h|cuvânt|1|dimensiunea antetului de bază|
|0004h|byte|1|Dimensiunea antetului|
|0005h|byte|1|Numărul versiunii arhivatorului|
|0006h|byte|1|Numărul minim al versiunii este necesar|
|0007h|byte|1|OS gazdă:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Sistem xx)</br> 5 - OS/2</br> 6 - MER GS</br> 7 - ATARI ST</br> 8 - Următorul</br> 9 - VAX VMS|
|0008h|byte|1|Semnale interne, bitmap:</br> 0 - fără parolă/parolă</br> 1 - rezervat</br> 2 - fișierul continuă pe următorul disc</br> 3 - câmpul pentru poziţia de pornire a fişierului este disponibil</br> 4 - traducerea căii ( "\" în "/" )|
|0009h|byte|1|Metoda de compresie:</br> 0 - stocat</br> 1 - comprimat cel mai mult</br> 2 - comprimat</br> 3 - comprimat mai repede</br> 4 - comprimat cel mai rapid|
|000Ah|byte|1|Tip de fișier:</br> 0 - binar</br> Text pe 1 - 7 biți</br> 2 - antet comentariu</br> 3 - director</br> 4 - etichetă de volum|
|000Bh|byte|1|rezervat|
|000Ch|dword|1|Data/Ora fișierului original în format MS-DOS|
|0010h|dword|1|Dimensiunea fișierului comprimat|
|0014h|dword|1|Dimensiunea fișierului original"|
|0018h|dword|1|CRC-32 al fișierului original|
|001Ah|cuvânt|1|Poziția fișierului în numele fișierului|
|001Ch|cuvânt|1|Atribute fișiere|
|001Eh|cuvânt|1|Date gazdă|
|?|dword|1|Poziția de pornire a fișierului extins|
|????h|dword|1|CRC-32 din antetul de bază|
|????h|cuvânt|1|Mărimea primului antet extins|
|????h+"SIZ"+2|dword|1|CRC-32 din antetul extins|
|????h+"SIZ"+6|byte|?|Fișier comprimat|

## Referințe ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

