---
date: 2019-10-11
keywords: srt, .srt, srt-filformat, .srt-filformat, .srt-tillägg, srt-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om SRT-filformat och API:er som kan skapa och öppna SRT-filer." 
title: SRT-filformat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Vad är en SRT fil? ##

SRT (SubRip-filformat) är en enkel undertextfil som sparas i filformatet SubRip med filtillägget .srt. Den innehåller ett sekventiellt antal undertexter, start- och sluttidsstämplar samt undertext. SRT-filer gör det möjligt att lägga till undertexter till videoinnehåll efter att det har producerats.

## SRT-filstruktur ##

Varje undertext har fyra delar i SRT-filen.

1. En numerisk räknare som anger numret eller positionen för undertexten.
1. Start- och sluttid för undertexten separerade med --> tecken
1. Undertext på en eller flera rader.
1. En tom rad som indikerar slutet på undertexten.

### Exempel på SRT ###

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

För att ange tiden används formatet *timmar:minuter:sekunder,millisekunder (00:00:00,000)*.

## Formatering av SRT-filer ##

Formateringen av SRT-filer kommer från HTML-taggar. Formateringstaggarna för SRT-filen listas nedan.

| Effekt | Taggar |
| --- | --- |
|Fet|**\ <b>...\</b> ** eller {b}...{/b}|
|Kursiv|**\ <i>...\</i> ** eller **{i}...{/i}**|
|Understrykning|**\ <u>...\</u> ** eller **{u}...{/u}**|
|Teckensnittsfärg|**\ <font color="white">...\</font> **|
|Linjeposition|**{\a3}** (anger att texten ska börja visas på rad 3)

## SubRip programvara ##

SubRip är ett gratisprogram som körs på Windows. Det extraherar undertexter och deras timings från olika videoformat och sparar undertexterna i SRT-format. SubRip använder optisk teckenigenkänning för att extrahera undertexter från livevideo, andra videofiler och DVD-skivor.

## Referenser ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
