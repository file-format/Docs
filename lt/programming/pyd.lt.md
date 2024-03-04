---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD failo formatas – Python Dynamic Module
linktitle: PYD
description: Luždirbti apie PYD failo formatą ir API, kurios gali sukurti ir atidaryti PYD failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Kas yra PYD failas?

PYD failas yra Python parašyta dinaminių saitų biblioteka, kurią vykdymo metu gali paleisti kitas Python kodas. Jame yra vienas ar daugiau Python modulių, kurie palengvina kodo pakartotinį naudojimą ir suteikia modulio architektūrą programoms rašyti. PYD failus galima sukurti ir išsaugoti su plėtiniu .pyd, pvz., helloworld.pyd. Programų kūrėjai gali naudoti importavimo teiginį, norėdami įtraukti PYD modulius į savo programas. PYD failus galima atidaryti naudojant Python Software Foundation Python, kuri yra prieinama Windows, Mac ir Linux OS.

## PYD failo formatas – daugiau informacijos

PYD failai parašyti Python programavimo kalba ir generuojami kompiliuojant Python kodą.

## Skirtumas tarp PY ir PYD failų formatų

[PY](/programming/py/) faile yra šaltinio kodas, kuris vykdomas toks, koks yra, ir negali būti įtrauktas kaip pakartotinai naudojamas kodas kitose Python programose. Tačiau PYD failas yra dinamiškai susieta biblioteka, skirta naudoti Windows operacinėje sistemoje.

## Kaip sukurti PYD failą?

PYD failą galima sukurti sukūrus modulį pavadinimu, pvz., exmaple.pyd. Šiame modulyje bus visos funkcijos vienos ar kelių funkcijų pavidalu, pvz., PyMod_example(). Kai programa apima šią biblioteką ir ją iškviečia, tai galima padaryti importuojant modulį ir bus paleista funkcija PyMod_example().

## Nuorodos Nr.

 * [Python plėtinių kūrimas naudojant C/C++](https://sebsauvage.net/python/mingw.html)
 * [Python (programavimo kalba) – Vikipedija](https://en.wikipedia.org/wiki/Python_(programming_language))

