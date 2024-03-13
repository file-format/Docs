---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LSRT faylı yarada və aça bilən SRT fayl formatı və API-lər haqqında qazanıns.
title: SRT fayl formasıat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## SRT faylı nədir? ##

SRT (SubRip fayl formatı) .srt uzantısı ilə SubRip fayl formatında saxlanılan sadə altyazı faylıdır. O, ardıcıl sayda altyazıları, başlanğıc və bitmə vaxtlarını və altyazı mətnini ehtiva edir. SRT faylları video məzmunu hazırlandıqdan sonra ona subtitrlər əlavə etməyə imkan verir.

## SRT fayl strukturu ##

Hər bir altyazı SRT faylında dörd hissədən ibarətdir.

1. Altyazının sayını və ya mövqeyini göstərən rəqəmsal sayğac.
1. Altyazının başlama və bitmə vaxtı --> simvolları ilə ayrılır
1. Bir və ya bir neçə sətirdə altyazı mətni.
1. Altyazının sonunu göstərən boş sətir.

### SRT nümunəsi ###

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

Vaxtı təyin etmək üçün *saat:dəqiqə:saniyə,millisaniyə (00:00:00,000)* formatından istifadə olunur.

## SRT fayllarının formatlanması ##

SRT fayllarının formatlanması HTML teqlərindən əldə edilir. SRT faylı üçün formatlama teqləri aşağıda verilmişdir.

| Effekt | Teqlər |
| --- | --- |
|Qalın|**\ <b>...\</b> ** və ya {b}...{/b}|
|Kursiv|**\ <i>...\</i> ** və ya **{i}...{/i}**|
|Altdan xətt çək|**\ <u>...\</u> ** və ya **{u}...{/u}**|
|Şrift Rəngi|**\ <font color=white>...\</font> **|
|Sətrin Mövqeyi|**{\a3}** (mətnin 3-cü sətirdə görünməyə başlamalı olduğunu göstərir)

## SubRip Proqramı ##

SubRip Windows-da işləyən pulsuz proqramdır. O, müxtəlif video formatlarından subtitrləri və onların vaxtlarını çıxarır və altyazıları SRT formatında saxlayır. SubRip canlı video, digər video faylları və DVD-lərdən altyazıları çıxarmaq üçün optik xarakter tanınmasından istifadə edir.

## İstinadlar ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
