---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LMP4 faylı yarada və aça bilən MP4 fayl formatı və API-lər haqqında qazanıns.
title: MP4 fayl formasıat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## MP4 faylı nədir? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Qısa tarix ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. MP4-ün ilk versiyası (ISO/IEC 14496-1:2001) 1999-cu ildə nəşr olunan MPEG-4 1-ci Hissə: Sistem spesifikasiyasına yenidən baxılmışdır. MP4 fayl formatı ISO Baza Media Fayl Formatında ISO/IEC 14496-12 üçün ümumiləşdirilmişdir. :2004, zamana əsaslanan media faylları üçün ümumi strukturu müəyyən etdi. Nəticədə, digər fayl formatları üçün əsas kimi istifadə olunur.

## MP4 Faylların Strukturu ##

MP4 genişləndirilə bilən konteyner faylıdır, yəni o, ciddi strukturu müəyyən etmir və hər bir media növü üçün fərdi struktur və iyerarxiyaya imkan verir. MP4 faylındakı məlumatlar iki hissəyə bölünür, birincisi media ilə əlaqəli məlumatları, ikincisi isə metaməlumatları ehtiva edir. Media məlumatlarında audio və ya video var və metadata təsadüfi giriş üçün bayraqları, vaxt ştamplarını və s.
MP4-dəki strukturlara adətən atomlar və ya qutular deyilir. Atomun minimum ölçüsü 8 baytdır (ilk 4 bayt ölçüsü, sonrakı 4 bayt isə növü müəyyən edir). MP fayllarında olan kök səviyyəli atomların siyahısı:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: Mütərəqqi video yükləmə/endirmə məlumatını ehtiva edir.
- **moov**: Bütün film metadataları üçün konteyner.
- **moof**: Video fraqmentləri olan konteyner.
- **mfra**: Video fraqmentinə təsadüfi girişi olan konteyner
- **mdat**: Media üçün məlumat konteyneri.
- **stts**: nümunə-vaxt cədvəli.
- **stsc**: nümunədən parçaya cədvəl.
- **stsz**: nümunə ölçüləri (çərçivələmə)
- **meta**: Metadata məlumatı olan konteyner.

MP4-də istifadə olunan ikinci səviyyəli atomların siyahısı:

- **mvhd**: Videonun tam təfərrüatları ilə video başlıq məlumatını ehtiva edir.
- **trak**: Fərdi treki olan konteyner.
- **udta**: İstifadəçi və izləmə məlumatı olan konteyner.
- **iods**: MP4 fayl deskriptoru

## İstinadlar ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

