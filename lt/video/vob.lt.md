---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie VOB failo formatą ir API, kurios gali sukurti ir atidaryti VOB failąs.
title: VOB failo formaat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Kas yra VOB failas? ##

VOB failai paprastai saugomi VIDEO_TS kataloge DVD diske su plėtiniu .vob. VOB failuose yra vaizdo ir garso duomenų bei kitų duomenų, tokių kaip meniu ir subtitrai. VOB yra pagrįstas MPEG-2 programų srauto formatu, tačiau jis turi papildomų apribojimų ir specifikacijų privačiuose srautuose. VOB failai yra griežtas MPEG programų srautų pogrupis, todėl visi VOB failai yra MPEG programų srautai, bet visi MPEG programų srautai nėra suderinami su VOB.

## DVD vaizdo struktūra ##

Kai kompiuteryje atidaromas DVD, VIDEO_TS yra aukščiausio lygio katalogas su AUDIO_TS. AUDIO_TS yra tuščias ir nenaudojamas. VIDEO_TS kataloge yra VOB, BUP ir IFO failai. VOB failuose yra MPEG turinio. Jie yra suskirstyti į 1 GB ar mažesnius gabalus, kad būtų suderinami su visomis operacinėmis sistemomis. IFO failuose yra informacija apie meniu ir pavadinimo struktūrą. BUK failai yra to paties pavadinimo IFO failų atsarginės kopijos. Šie failai skirti fiziškai laikyti atskiroje vietoje, kad jei IFO failas būtų sugadintas dėl fizinės DVD sugadinimo, BUK failas galėtų pateikti tą pačią informaciją.

### Fizinis išdėstymas ###

- Visi diske esantys failai turi būti gretimi.
- Susiję failai turi būti vienas šalia kito (VOB, IFO, BUP).
- Sunumeruoti failai turi būti didėjimo tvarka.

## Apsauga nuo kopijavimo ##

Daugelis vaizdo DVD yra užšifruoti ir neleidžia kopijuoti duomenų iš DVD. Autentifikavimo ir iššifravimo raktai reikalingi norint paleisti failus, esančius nepasiekiamoje DVD įvesties srityje. Šiuos raktus naudoja CSS iššifravimo programinė įranga, kuri yra DVD grotuve arba programinės įrangos grotuve. Be klavišų vaizdo įrašų failai negali būti paleisti, nes atidarant failus bus paprašyta klavišų.

## Nuorodos Nr.

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

