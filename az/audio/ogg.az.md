---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LOGG fayl formatı və OGG faylını yarada və aça bilən API-lər haqqında qazanıns.
title: OGG Faylı - Ogg Vorbis Audio File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## OGG faylı nədir?

OGG .ogg uzantısı ilə saxlanılan Ogg Vorbis Sıxılmış Audio Faylıdır. OGG faylları audio məlumatların saxlanması üçün istifadə olunur və onlara rəssam və trek məlumatı və metadata da daxil ola bilər. OGG Xiph.Org Fondu tərəfindən qorunan pulsuz və açıq konteyner formatıdır.

## OGG Fayl Formatının Qısa Tarixi

Ogg layihəsi 1993-cü ildə daha böyük bir layihənin bir hissəsi olaraq başladı və Squish adlandırıldı, lakin mövcud ticarət nişanına görə OggSquish olaraq adlandırıldı. Bu, müasir audio proqramları üçün çevik sıxılmış audio formatı yaratmaq cəhdi kimi təsvir edilmişdir. OGG arayışı 2 sentyabr 2000-ci ildə Vorbisdən ayrıldı.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. 30 iyun 2009-cu ilə qədər OGG Firefox 3.5-in HTML5 tətbiqi ilə dəstəklənən yeganə konteyner formatı idi.

## OGG fayl formatı

OGG formatı məlumat parçalarından ibarətdir. Hər bir parça Ogg səhifəsi adlanır. Ogg Formatını müəyyən etmək üçün hər bir səhifə OggS ilə başlayır. Başlıqda hər bir səhifəni seriyanın bir hissəsi kimi müəyyən edən seriya nömrəsi və səhifə nömrəsi var. Səhifə aşağıdakı komponentlərdən ibarətdir.

- **Səhifə Başlığı**
  - "**Capture Pattern(32 bits)**: Bu OGG fayllarını təhlil edərkən sinxronizasiya üçün istifadə olunur."
  - "**Versiya(8 bit)**: Ogg bit axınının versiyasını göstərir."
  - "**Başlıq Tipi(8 bit)**: Səhifənin növünü göstərir."

| Bit | Dəyər | Təsvir |
| --- | --- | --- |
| 0 | 0x01 | Səhifənin ilk paketinin məntiqi bit axınında əvvəlki paketin davamı olduğunu göstərir. |
| 1 | 0x02 | Bu səhifənin məntiqi bit axınında birinci olduğunu göstərir. |
| 2 | 0x04 | Bu səhifənin məntiqi bit axınında sonuncu olduğunu göstərir. |

  - "**Qranulun yeri(64 bit)**: Bu, mənası kodek tərəfindən müəyyən edilən vaxt işarəsidir."
  - "**Bitstream seriya nömrəsi(32 bit)**: Bu, müəyyən məntiqi bit axınına aid səhifəni müəyyən edən seriya nömrəsidir."
  - "**Səhifə ardıcıllığının nömrəsi(32 bit)**: İlk səhifə 0-dan başlayan səhifənin ardıcıllığını göstərir."
  - "**Baxma məbləği(32 bit)**: Bütün səhifə məlumatlarının CRC32 yoxlama cəmini təmin edir."
  - "**Səhifə seqmentləri(8 bit)**: Səhifədəki seqmentlərin sayını göstərir."
  - "**Seqment cədvəli**: Səhifənin gövdəsindəki hər bir seqmentin uzunluğunu göstərən 8 bitlik dəyərlər massividir."
- **Metaməlumat**: VorbisComment metadata saxlamaq üçün ən geniş dəstəklənən mexanizmdir. Digər mexanizmlərə aşağıdakılar daxildir:
  - "FLAC metadata blokları"
  - "Ogg Skeleton"
  - "Davamlı Media İşarələmə Dili"

## İstinadlar ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

