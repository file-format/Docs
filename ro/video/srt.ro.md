---
date: 2019-10-11
keywords: srt, .srt, format de fișier srt, format de fișier .srt, extensie .srt, extensie srt
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier SRT și despre API-urile care pot crea și deschide fișiere SRT."
title: Format de fișier SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Ce este un fișier SRT? ##

SRT (formatul de fișier SubRip) este un fișier simplu de subtitrare salvat în formatul de fișier SubRip cu extensia .srt. Conține un număr succesiv de subtitrări, marcaje temporale de început și de sfârșit și text de subtitrare. Fișierele SRT fac posibilă adăugarea de subtitrări la conținutul video după ce acesta este produs.

## Structura fișierului SRT ##

Fiecare subtitrare are patru părți în fișierul SRT.

1. Un numărător numeric care indică numărul sau poziția subtitrului.
1. Ora de început și de sfârșit a subtitrarii separate prin --> caractere
1. Subtitrarea textului pe una sau mai multe rânduri.
1. O linie goală care indică sfârșitul subtitrului.

### Exemplu de SRT ###

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

Pentru a specifica timpul, este utilizat formatul *ore:minute:secunde,milisecunde (00:00:00,000).

## Formatarea fișierelor SRT ##

Formatarea fișierelor SRT este derivată din etichetele HTML. Etichetele de formatare pentru fișierul SRT sunt enumerate mai jos.

| Efect | Etichete |
| --- | --- |
|Aldin|**\ <b>...\</b> ** sau {b}...{/b}|
|Italic|**\ <i>...\</i> ** sau **{i}...{/i}**|
|Subliniați|**\ <u>...\</u> ** sau **{u}...{/u}**|
|Culoarea fontului|**\ <font color="white">...\</font> **|
|Poziția liniei|**{\a3}** (indică faptul că textul ar trebui să înceapă să apară pe linia 3)

## Software SubRip ##

SubRip este un program software gratuit care rulează pe Windows. Extrage subtitrările și sincronizarea acestora din diferite formate video și salvează subtitrările în format SRT. SubRip folosește recunoașterea optică a caracterelor pentru a extrage subtitrări din videoclipuri live, alte fișiere video și DVD-uri.

## Referințe ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
