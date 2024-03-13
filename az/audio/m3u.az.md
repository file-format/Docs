---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LM3U fayl formatını və M3U faylını yarada və aça bilən API-lər haqqında qazanıns.
title: M3U Fayl Formasıat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## M3U faylı nədir? ##

M3U (MP3 URL) .m3u uzantısı ilə saxlanılan audio pleylist faylıdır. M3U faktiki audio fayl deyil, sadəcə audio və bəzən video faylları göstərir. M3U Fraunhofer tərəfindən Winplay3 proqramı ilə istifadə edilmək üçün hazırlanmışdır. O, həmçinin müxtəlif media pleyerləri və proqram təminatı tərəfindən dəstəklənir.

## M3U fayl formatı

M3U fayl formatı üçün rəsmi spesifikasiya yoxdur, bu, faktiki standartdır. M3U, mətn yerli sistemin standart qeyri-Unicode kodlaşdırmasında kodlaşdırılıbsa, .m3u genişlənməsindən və ya mətn UTF-8 ilə kodlaşdırılıbsa, .m3u8 uzantısından istifadə edən düz mətn faylıdır. M3U faylındakı hər bir giriş aşağıdakılardan biri ola bilər:

- Fayl üçün mütləq yol
- M3U faylına nisbətən fayl yolu.
- URL

### Genişləndirilmiş M3U ###

Genişləndirilmiş M3U-da # ilə başlayan və parametrləri varsa iki nöqtə (:) ilə bitən əlavə direktivlər təqdim olunur. Aşağıda genişləndirilmiş M3U üçün direktivlərin siyahısı verilmişdir.

- **#EXTM3U** - Genişləndirilmiş M3U-nu göstərən fayl başlığıdır və faylın birinci sətri olmalıdır.
- **#EXTENC:** - Mətnin kodlaşdırılması. Faylın 2-ci sətri olmalıdır.
- **#EXTINF:** - Track məlumatı və digər əlavə xüsusiyyətlər üçün istifadə olunur.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Ad qruplaşdırmağa başlayın
- **#EXTALB:** - Albom haqqında məlumat
- **#EXTART:** - Albom rəssamı
- **#EXTGENRE** - Albom Janrı
- **#EXTM3A** - Albom parçaları və ya fəsillər üçün tək fayl pleylist.
- **#EXTBYT:** - Fayl ölçüsü baytla.
- **#EXTBIN:** - İkili verilənlər aşağıdakılardır.
- **#EXTIMG:** - Loqo, Qapaq və ya digər şəkillər.

### HLS M3U ###

HLS (HTTP Live Streaming) Apple tərəfindən iOS cihazlarına audio və radio yayımı üçün yaradılmışdır. O, UTF-8 kodlu genişləndirilmiş M3U-ya əsaslanır. 2017-ci ildə IETF tərəfindən RFC 8216 kimi standartlaşdırıldı. HLS çalğı siyahısı üçün etiketlər #EXT-X- ilə başlayır. Aşağıda HLS üçün etiketlərin siyahısı verilmişdir

- **EXT-X-VERSION** - Media və onun serverinə əsaslanan faylın uyğunluq versiyasını göstərir.
- **#EXT-X-START:** - Pleylist üçün üstünlük verilən başlanğıc nöqtəsini göstərir.
- **#EXT-X-PLAYLIST-TYPE:** - Pleylist növünü təmin edir (OLAY və ya VOD).
- **#EXT-X-TARGETDURATION:** - Maksimum Seqment müddətini təyin edir.
- **#EXT-X-MEDIA-SEQUENCE:** - Media Sequence Number göstərir.
- **#EXT-X-MÜSTƏQİL-SEQMENTLƏR** - Bu, bütün media nümunələrinin müstəqil olduğunu və digər seqmentlər olmadan deşifrə edilə biləcəyini göstərir.
- **#EXT-X-MEDIA:** - Eyni məzmunun alternativ Renditionlarını ehtiva edən Media Playlistləri əlaqələndirmək üçün istifadə olunur.
- **#EXT-X-STREAM-INF:** - O, Təfsirlərin bir hissəsi olan Variant Yayımını müəyyən edir.
- **#EXT-X-BYTERANGE:** - Media Seqmentinin onun URI-si ilə müəyyən edilmiş resursun alt diapazonu olduğunu göstərir.
- **#EXT-X-DISCONTINUITY** - Əvvəlki və sonrakı media seqmentləri arasındakı fasiləni göstərir.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - O, eyni Variant Axının və ya müxtəlif Variant Axınlarının müxtəlif rendisiyaları arasında sinxronizasiyaya imkan verir.
- **#EXT-X-KEY:** - Media Seqmentlərinin şifrəsinin necə açılacağını müəyyənləşdirir.
- **#EXT-X-MAP:** - Media Initialization Bölməsinin necə əldə olunacağını müəyyənləşdirir. Tətbiq olunan Media Seqmentlərini təhlil etmək tələb olunur.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - Məlumat diapazonunu əlaqələndirir.
- **#EXT-XI-FRAMES-ONLY** - Pleylistdəki hər bir Media Seqmentinin tək I-çərçivəni təsvir etdiyini göstərir.
- **EXT-XI-FRAME-STREAM-INF** - Bu, pleylist faylında Multimedia təqdimatının I-çərçivəsində olduğunu göstərir.
- **#EXT-X-SESSION-DATA:** - Bu, ixtiyari sessiya məlumatlarının olmasına imkan verir
Master Playlist-də keçirilir.
- **#EXT-X-SESSION-KEY:** - Şifrələmə açarlarına imkan verir. Müştəri əvvəlcə çalğı siyahısını oxumadan bu düymələri əvvəlcədən yükləyə bilər.
- **#EXT-X-ENDLIST** - Bu, fayla daha Media Seqmentlərinin əlavə olunmayacağını bildirir.

Aşağıda M3U tərəfindən istifadə edilən İnternet media növlərinin siyahısı verilmişdir:

- **application/vnd.apple.mpegurl**: Bu, HLS proqramlarında çalğı siyahılarına istinad etmək üçün istifadə edilən M3U üçün yeganə qeydə alınmış media növüdür (2009-cu ildə qeydiyyatdan keçmişdir).
- Aşağıdakı İnternet media növləri qeyri-HLS proqramları tərəfindən istifadə olunur.
  - "**tətbiq/mpegurl**"
  - "**tətbiq/x-mpegurl**"
  - "**audio/mpegurl**"
  - "**audio/x-mpegurl**"

## M3U Nümunəsi ##

Bu M3U faylının bir nümunəsidir.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## İstinadlar ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

