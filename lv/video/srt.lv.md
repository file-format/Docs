---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par SRT faila formātu un API, kas var izveidot un atvērt SRT failus.
title: SRT faila veidlapaat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Kas ir SRT fails? ##

SRT (SubRip faila formāts) ir vienkāršs subtitru fails, kas saglabāts SubRip faila formātā ar paplašinājumu .srt. Tas satur secīgu skaitu subtitru, sākuma un beigu laikspiedolu un subtitru tekstu. SRT faili ļauj pievienot subtitrus video saturam pēc tā izgatavošanas.

## SRT faila struktūra ##

Katram apakšvirsrakstam SRT failā ir četras daļas.

1. Ciparu skaitītājs, kas norāda subtitru numuru vai pozīciju.
1. Subtitru sākuma un beigu laiks atdalīts ar --> rakstzīmēm
1. Subtitru teksts vienā vai vairākās rindās.
1. Tukša rindiņa, kas norāda subtitru beigas.

### SRT piemērs ###

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

Lai norādītu laiku, tiek izmantots formāts *stundas:minūtes:sekundes,milisekundes (00:00:00,000)*.

## SRT failu formatēšana ##

SRT failu formatējums tiek iegūts no HTML tagiem. Tālāk ir norādīti SRT faila formatēšanas tagi.

| Efekts | Birkas |
| --- | --- |
|Bold|**\ <b>...\</b> ** vai {b}...{/b}|
|Italic|**\ <i>...\</i> ** vai **{i}...{/i}**|
|Pasvītrot|**\ <u>...\</u> ** vai **{u}...{/u}**|
|Fonta krāsa|**\ <font color=white>...\</font> **|
|Line Position|**{\a3}** (norāda, ka tekstam jāsāk parādīties 3. rindiņā)

## SubRip programmatūra ##

SubRip ir bezmaksas programmatūra, kas darbojas operētājsistēmā Windows. Tas izvelk subtitrus un to laikus no dažādiem video formātiem un saglabā subtitrus SRT formātā. SubRip izmanto optisko rakstzīmju atpazīšanu, lai iegūtu subtitrus no tiešraides video, citiem video failiem un DVD.

## Atsauces Nr.

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
