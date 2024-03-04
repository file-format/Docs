---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ failo formaat
linktitle: ARJ
description: Luždirbti apie ARJ failo formatą ir API, kurios gali sukurti ir atidaryti ARJ failąs.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Kas yra ARJ failas? ##

ARJ (archyvuotas Robert Jung) yra didelio efektyvumo suspaustas archyvo failas, kurį sukūrė Robertas K. Jungas. ARJ buvo sukurtas DOS ir ankstyvosioms Windows versijoms 1990-ųjų pradžioje. ARJ failai yra naudingi kuriant atsargines kopijas arba bendrinant daug failų, nes jums nereikia sekti visų tų failų, o tvarkyti reikia tik vieną failą. Plėtinys .arj naudojamas ARJ archyvo failams.

## ARJ failo formatas ##

ARJ faile yra dviejų tipų antraštės:

- Pagrindinė antraštė: archyvo pradžioje yra viena pagrindinė antraštė.
- Vietinės antraštės: vietinės antraštės yra prieš kiekvieną failą.

|Poslinkis|Tipas|Skaičius|Aprašymas|
|---|---|---|---|
|0000h|žodis|1|ID=0EA60h|
|0002h|žodis|1|pagrindinis antraštės dydis|
|0004h|baitas|1|Antraštės dydis|
|0005h|baitas|1|Archyvo versijos numeris|
|0006h|baitas|1|Reikalingas minimalus versijos numeris|
|0007h|baitas|1|Pagrindinės OS:</br> 0 – MS-DOS</br> 1 - PRIMOS</br> 2 – UNIX</br> 3 - AMIGA</br> 4 – MAC-OS (System xx)</br> 5 – OS/2</br> 6 - APPLE GS</br> 7 - ATARI g</br> 8 – KITAS</br> 9 - VAX VMS|
|0008h|baitas|1|Vidinės vėliavėlės, su bitais:</br> 0 - nėra slaptažodžio / slaptažodžio</br> 1 - rezervuotas</br> 2 - failas tęsiasi kitame diske</br> 3 – yra failo pradžios padėties laukas</br> 4 - kelio vertimas ( \ į / )|
|0009h|baitas|1|Suspaudimo metodas:</br> 0 – saugomas</br> 1 – labiausiai suspaustas</br> 2 - suspaustas</br> 3 – greičiau suspaustas</br> 4 - suspaustas greičiausiai|
|000Ah|baitas|1|Failo tipas:</br> 0 – dvejetainis</br> 1–7 bitų tekstas</br> 2 – komentaro antraštė</br> 3 - katalogas</br> 4 - tomo etiketė|
|000Bh|baitas|1|rezervuotas|
|000Ch|dword|1|Pirminio failo data/laikas MS-DOS formatu|
|0010h|dword|1|Suglaudinto failo dydis|
|0014h|dword|1|Pradinio failo dydis|
|0018h|dword|1|pirminio failo CRC-32|
|001Ah|word|1|Failo specifikacijos vieta failo pavadinime|
|001Ch|word|1|Failo atributai|
|001Eh|word|1|Pagrindinio kompiuterio duomenys|
|?|dword|1|Išplėstinė failo pradinė padėtis|
|????h|dword|1|pagrindinės antraštės CRC-32|
|????h|word|1|Pirmosios išplėstinės antraštės dydis|
|????h+SIZ+2|dword|1|CRC-32 išplėstinės antraštės|
|????h+SIZ+6|baitas|?|Suspaustas failas|

## Nuorodos Nr.

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

