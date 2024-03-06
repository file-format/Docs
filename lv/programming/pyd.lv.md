---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD faila formāts — Python Dynamic Module
linktitle: PYD
description: Lnopelniet par PYD faila formātu un API, kas var izveidot un atvērt PYD failus.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Kas ir PYD fails?

PYD fails ir Python rakstīta dinamisko saišu bibliotēka, kuru izpildes laikā var palaist cits Python kods. Tajā ir viens vai vairāki Python moduļi, kas atvieglo koda atkārtotu izmantošanu un nodrošina moduļu arhitektūru lietojumprogrammu rakstīšanai. PYD failus var izveidot un saglabāt ar .pyd paplašinājumu, piemēram, helloworld.pyd. Lietojumprogrammu izstrādātāji var izmantot importēšanas paziņojumu, lai savās lietojumprogrammās iekļautu PYD moduļus. PYD failus var atvērt, izmantojot Python Software Foundation Python, kas ir pieejama operētājsistēmām Windows, Mac un Linux OS.

## PYD faila formāts — vairāk informācijas

PYD faili ir rakstīti Python programmēšanas valodā un tiek ģenerēti, apkopojot Python kodu.

## Atšķirība starp PY un PYD failu formātiem

Fails [PY](/programming/py/) satur avota kodu, kas tiek izpildīts tāds, kāds tas ir, un to nevar iekļaut kā atkārtoti lietojamu kodu citās Python lietojumprogrammās. Tomēr PYD fails ir dinamiski saistīta bibliotēka, kas jāizmanto operētājsistēmā Windows.

## Kā izveidot PYD failu?

PYD failu var izveidot, izveidojot moduli ar nosaukumu, piemēram, exmaple.pyd. Šajā modulī būs visas funkcionalitātes vienas vai vairāku funkciju veidā, piemēram, PyMod_example(). Kad programma ietver šo bibliotēku un to izsauc, to var izdarīt, importējot moduli un darbosies funkcija PyMod_example().

## Atsauces Nr.

 * [Python paplašinājumu izveide programmā C/C++](https://sebsauvage.net/python/mingw.html)
 * [Python (programmēšanas valoda) — Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

