---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie SRT failo formatą ir API, kurios gali sukurti ir atidaryti SRT failąs.
title: SRT failo formaat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Kas yra SRT failas? ##

SRT (SubRip failo formatas) yra paprastas subtitrų failas, įrašytas SubRip failo formatu su plėtiniu .srt. Jame yra nuoseklus subtitrų skaičius, pradžios ir pabaigos laiko žymos ir subtitrų tekstas. SRT failai leidžia pridėti subtitrus prie vaizdo įrašo turinio jį pagaminus.

## SRT failo struktūra ##

Kiekvienas subtitras turi keturias dalis SRT faile.

1. Skaitmeninis skaitiklis, rodantis subtitrų skaičių arba vietą.
1. Subtitrų pradžios ir pabaigos laikas atskirtas --> simboliais
1. Subtitrų tekstas vienoje ar daugiau eilučių.
1. Tuščia eilutė, nurodanti subtitrų pabaigą.

### SRT pavyzdys ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Norint nurodyti laiką, naudojamas formatas *valandos:minutės:sekundės,milisekundės (00:00:00,000)*.

## SRT failų formatavimas ##

SRT failų formatavimas gaunamas iš HTML žymų. SRT failo formatavimo žymos pateiktos žemiau.

| Efektas | Žymos |
| --- | --- |
|Paryškintas|**\ <b>...\</b> ** arba {b}...{/b}|
|Italic|**\ <i>...\</i> ** arba **{i}...{/i}**|
|Pabraukimas|**\ <u>...\</u> ** arba **{u}...{/u}**|
|Šrifto spalva|**\ <font color=white>...\</font> **|
|Eilutės padėtis|**{\a3}** (rodo, kad tekstas turėtų būti rodomas 3 eilutėje)

## SubRip programinė įranga ##

SubRip yra nemokama programinė įranga, veikianti Windows. Jis išskiria subtitrus ir jų laiką iš skirtingų vaizdo formatų ir išsaugo subtitrus SRT formatu. SubRip naudoja optinį simbolių atpažinimą, kad ištrauktų subtitrus iš tiesioginio vaizdo, kitų vaizdo failų ir DVD.

## Nuorodos Nr.

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
