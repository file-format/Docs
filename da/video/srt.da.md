---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om SRT filformat og API'er, der kan oprette og åbne SRT fils.
title: SRT fil formularat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Hvad er en SRT fil? ##

SRT (SubRip-filformat) er en simpel undertekstfil, der er gemt i SubRip-filformatet med filtypenavnet .srt. Den indeholder et sekventielt antal undertekster, start- og sluttidsstempler og underteksttekst. SRT-filer gør det muligt at tilføje undertekster til videoindhold, efter det er produceret.

## SRT-filstruktur ##

Hver undertekst har fire dele i SRT-filen.

1. En numerisk tæller, der angiver nummeret eller placeringen af underteksten.
1. Start- og sluttidspunkt for underteksten adskilt af --> tegn
1. Underteksttekst i en eller flere linjer.
1. En tom linje, der angiver slutningen af underteksten.

### Eksempel på SRT ###

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

For at angive tiden bruges formatet *timer:minutter:sekunder,millisekunder (00:00:00.000)*.

## Formatering af SRT-filer ##

Formateringen af SRT-filer er afledt af HTML-tags. Formateringsmærkerne for SRT-filen er angivet nedenfor.

| Effekt | Tags |
| --- | --- |
|Fed|**\ <b>...\</b> ** eller {b}...{/b}|
|Kursiv|**\ <i>...\</i> ** eller **{i}...{/i}**|
|Understregning|**\ <u>...\</u> ** eller **{u}...{/u}**|
|Skriftfarve|**\ <font color=white>...\</font> **|
|Linjeposition|**{\a3}** (angiver, at teksten skal begynde at blive vist på linje 3)

## SubRip Software ##

SubRip er et gratis softwareprogram, der kører på Windows. Den udtrækker undertekster og deres timings fra forskellige videoformater og gemmer underteksterne i SRT-format. SubRip bruger optisk tegngenkendelse til at udtrække undertekster fra live video, andre videofiler og dvd'er.

## Referencer ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
