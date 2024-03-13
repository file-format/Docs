---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LF4V fayl formatını və F4V faylını yarada və aça bilən API-lər haqqında qazanınes
title: F4V fayl formasıat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## F4V faylı nədir? ##

F4V (Flash MP4 Video Faylı) .f4v uzantısı ilə saxlanılan video fayldır. O, ISO əsas media fayl formatına (MPEG-4 Part 12) əsaslanır. O, [MP4](/video/mp4/) ilə çox oxşardır, buna görə də qeyri-rəsmi olaraq Flash MP4 adlandırılır. [FLV](/video/flv/) H.264/ACC məzmununu yayımlayarkən məhdudiyyətlərə malik idi və nəticədə Adobe Systems yeni F4V formatını yaratdı. Flash Player, Flash Player 9 Update 3-ün buraxılışından bəri F4V fayllarını oynaya bilər.

## F4V fayllarının strukturu ##

F4V fayl formatı ISO əsas media fayl formatına (MPEG-4 Part 12) əsaslanır və MP4 formatına çox oxşardır. Strukturla bağlı təfərrüatlar üçün [MP4](/video/mp4/) səhifəsinə baxın. F4V və MP4 arasındakı əsas fərq F4V-nin saxlaya biləcəyi metadata formatlarıdır. Aşağıda F4V formatı tərəfindən dəstəklənən metadata formatlarının siyahısı verilmişdir.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP Metadata qutusu**: Bu qutu Film (moov) qutusundan dərhal sonra gəlir. Bununla, fayl XMP metadatasını ActionScript vasitəsilə SWF filminə ötürə bilər.
- **ilst box**: Bu qutu Meta (meta) qutunun içərisində olur və bir sıra metadata teqlərini ehtiva edə bilər. Dəstəklənən məlumat növləri aşağıda verilmişdir.
  - "**0**: Fərdi Məlumat."
  - "**1**: Mətn Məlumatı."
  - "**12, 14**: İkili Məlumat"
  - "**21**: Ümumi Məlumat."
- **Mətn İzləmə Metaməlumat qutusu**: Media Databox (mdat) daxilində mətn nümunələri (mətn və ya tx3g). O, aşağıdakı metadata qutularını ehtiva edə bilər.
  - "**Üslub qutusu**: Mətn üslubunun spesifikasiyası."
  - "**Vurğulama qutusu**: Vurğulanacaq mətnin diapazonunu müəyyən edir."
  - "**Vurğulanan Rəng qutusu**: Mətn üçün vurğu rəngini təyin edir."
  - "**Karaoke qutusu**: Karaoke metadatasını göstərdi."
  - "**Scroll Delay qutusu**: Sürüşmə gecikməsini təyin edir."
  - "**Drop Shadow Ofset qutusu**: Mətn üçün aşağı kölgə ofset koordinatlarını təyin edir."
  - "**Drop Shadow Alpha qutusu**: Mətn üçün kölgə alfa dəyərini təyin edir."
  - "**Hipermətn qutusu**: Mətn diapazonunda alt mətnlə hipermətn mətnini təyin edir."
  - "**Mətn qutusu**: Mətn qutusu üçün koordinatları müəyyən edir."
  - "**Yanıb-sönən qutu**: Bir sıra mətn üçün yanıb-sönməni təyin edir."
  - "**Mətn Sarma qutusu**: Mətn üçün mətn sarğı bayrağını təyin edir."
  - "**Mətn Sarma qutusu**: Mətn üçün mətn sarğı bayrağını təyin edir."

## İstinadlar ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

