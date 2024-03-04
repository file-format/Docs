---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie F4V failo formatą ir API, kurios gali sukurti ir atidaryti F4V failąes
title: F4V failo formaat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Kas yra F4V failas? ##

F4V (Flash MP4 Video File) yra vaizdo failas, išsaugotas su plėtiniu .f4v. Jis pagrįstas ISO baziniu medijos failo formatu (MPEG-4 12 dalis). Jis labai panašus į [MP4](/video/mp4/), todėl neoficialiai dar vadinamas Flash MP4. [FLV](/video/flv/) turėjo apribojimų perduodant H.264/ACC turinį, todėl Adobe Systems sukūrė naują F4V formatą. Flash Player gali atkurti F4V failus nuo Flash Player 9 naujinimo 3 išleidimo.

## F4V failų struktūra ##

F4V failo formatas yra pagrįstas ISO baziniu medijos failo formatu (MPEG-4 12 dalis) ir yra labai panašus į MP4 formatą. Norėdami gauti daugiau informacijos apie struktūrą, žr. [MP4](/video/mp4/) puslapį. Pagrindinis skirtumas tarp F4V ir MP4 yra metaduomenų formatai, kuriuos F4V gali saugoti. Toliau pateikiamas metaduomenų formatų, kuriuos palaiko F4V formatas, sąrašas.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP metaduomenų laukelis**: šis laukelis pateikiamas iškart po langeliu Filmas (moov). Tokiu būdu failas gali perduoti XMP metaduomenis SWF filmui per ActionScript.
- **ilst box**: šis laukelis yra meta (meta) laukelyje ir jame gali būti daugybė metaduomenų žymų. Palaikomi duomenų tipai pateikti toliau.
  - "**0**: tinkinti duomenys."
  - "**1**: tekstiniai duomenys."
  - "**12, 14**: dvejetainiai duomenys"
  - "**21**: bendrieji duomenys."
– **Teksto takelio metaduomenų laukelis**: teksto pavyzdžiai (tekstas arba tx3g) medijos duomenų laukelyje (mdat). Jame gali būti šie metaduomenų laukeliai.
  - "**Stiliaus langelis**: teksto stiliaus specifikacijos."
  - "**Paryškinimo laukelis**: nurodo paryškinamo teksto diapazoną."
  - "**Paryškinimo spalvos laukelis**: nurodo teksto paryškinimo spalvą."
  - "**Karaoke dėžutė**: nurodyti karaokės metaduomenys."
  - "**Slinkties delsos laukelis**: nurodo slinkties delsą."
  - "**Šešėlio poslinkio laukelis**: nurodo teksto šešėlio poslinkio koordinates."
  - "**Drop Shadow Alpha box**: nurodo teksto šešėlio alfa reikšmę."
  - "**Hiperteksto laukelis**: nurodo hiperteksto tekstą su alternatyviuoju tekstu teksto diapazone."
  - "**Teksto laukelio laukelis**: apibrėžia teksto laukelio koordinates."
  - "**Mirksintis laukelis**: nurodomas tam tikro teksto diapazono mirksėjimas."
  - "**Teksto vyniojimo laukelis**: nustato teksto vyniojimo vėliavėlę."
  - "**Teksto vyniojimo laukelis**: nustato teksto vyniojimo vėliavėlę."

## Nuorodos Nr.

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

