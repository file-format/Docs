---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LVOB fayl formatı və VOB faylını yarada və aça bilən API-lər haqqında məlumat əldə edins.
title: VOB fayl formasıat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## VOB faylı nədir? ##

VOB faylları adətən .vob uzantısı olan DVD-də VIDEO_TS kataloqunda saxlanılır. VOB faylları video və audio məlumatları, eləcə də menyular və alt yazılar kimi digər məlumatları ehtiva edir. VOB MPEG-2 proqram axını formatına əsaslanır, lakin onun özəl axınlarda əlavə məhdudiyyətləri və spesifikasiyası var. VOB faylları MPEG proqram axınlarının ciddi alt çoxluğudur, buna görə də bütün VOB faylları MPEG proqram axınlarıdır, lakin bütün MPEG proqram axınları VOB ilə uyğun gəlmir.

## DVD Videonun strukturu ##

DVD kompüterdə açıldıqda, VIDEO_TS AUDIO_TS ilə üst səviyyəli kataloqdur. AUDIO_TS boşdur və istifadə edilmir. VIDEO_TS kataloqunun daxilində VOB, BUP və IFO faylları var. VOB faylları MPEG məzmununu ehtiva edir. Bunlar 1 GB və ya daha az ölçülü hissələrə bölünür ki, bütün əməliyyat sistemləri ilə uyğun olsun. IFO faylları menyular və başlıq strukturu ilə bağlı məlumatları ehtiva edir. BUK faylları eyni adlı IFO fayllarının ehtiyat nüsxəsidir. Bu faylların fiziki olaraq ayrı bir sahədə saxlanması nəzərdə tutulur ki, IFO faylı DVD-nin fiziki zədələnməsi səbəbindən zədələnərsə, BUK faylı eyni məlumatı təmin edə bilsin.

### Fiziki Plan ###

- Diskdəki bütün fayllar bitişik olmalıdır.
- Əlaqədar fayllar bir-birinin yanında olmalıdır (VOB, IFO, BUP).
- Nömrələnmiş fayllar artan ardıcıllıqla olmalıdır.

## Kopyalamadan qorunma ##

Bir çox video DVD-lər şifrələnir və məlumatların DVD-dən kopyalanmasının qarşısını alır. Doğrulama və şifrə açma açarları DVD-nin əlçatmaz giriş sahəsində yerləşən faylları oynamaq üçün lazımdır. Bu açarlar DVD pleyerdə və ya proqram pleyerində mövcud olan CSS deşifrə proqramı tərəfindən istifadə olunur. Düymələr olmadan video faylları oynatmaq mümkün deyil, çünki fayllar açıldığında düymələr tələb olunacaq.

## İstinadlar ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

