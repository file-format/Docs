---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR fayl formasıat
linktitle: JXR
description: LJXR fayl formatı və JXR faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## JXR faylı nədir? ##

JPEG XR (JPEG genişləndirilmiş diapazon) davamlı tonlu foto şəkillər üçün fayl formatıdır. Bu, Microsoft tərəfindən hazırlanmış HD Photo-a əsaslanan hərəkətsiz görüntü sıxılma standartıdır. Həm itkili, həm də itkisiz sıxılmanı dəstəkləyir.

## Qısa tarix ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. 2006-cı ilin noyabrında onun adı HD Photo olaraq dəyişdirildi. JPEG XR 19 iyun 2009-cu ildə ISO/IEC 29199-2 Beynəlxalq Standartı kimi təsdiq edildi. ITU-T və ISO/IEC hərəkət formatı spesifikasiyasını nəşr etdi (ITU-T T.833 | ISO/ IEC 29199-3), uyğunluq test dəsti (ITU-T T.834 | ISO/IEC 29199-4) və tamamlandıqdan sonra JPEG XR üçün istinad proqramı (ITU-T T.835 | ISO/IEC 29199-5) JPEG XR üçün iş axını arxitekturasını təsvir edən texniki hesabat 2011-ci ildə nəşr edilmişdir.

## JPEG XR Dizayn ##

JPEG ilə müqayisədə JPEG XR bir sıra təkmilləşdirmələr təklif edir:

- **Daha yaxşı sıxılma**: JPEG XR daha yüksək sıxılma nisbətləri təklif edir.
- **İtkisiz sıxılma**: JPEG XR itkisiz sıxılmanı dəstəkləyir.
- **Kafel Strukturu**: JPEG XR təsviri hər bir bölgənin ayrıca deşifrə oluna biləcəyi kafel bölgələrinə bölünə bilər.
- **Daha çox rəng dəqiqliyi**: JPEG XR, RGB rəng məkanından istifadə edərək şəkilləri dəstəkləmək üçün YCoCg rəng məkanına daxili çevrilmə daxildir. JPEG XR həmçinin hər bir komponent üçün 16 bitlik (piksel başına 64 bit) tam ədəd CMYK rəng modelini dəstəkləyir. JPEG XR HDR şəkilləri üçün RGBE paylaşılan eksponent üzən nöqtə rəng formatını dəstəkləyir. JPEG XR, həmçinin boz şkalası və çoxkanallı rəng kodlamasını dəstəkləyir.
- **Şəffaflıq Xəritəsi**: JPEG XR şəffaflıq üçün alfa kanalını dəstəkləyir.
- **Sıxılmış domen təsvirinin modifikasiyası**: JPEG XR şəkilləri itkili kodlaşdırmaya çevrilə, ayırdetmə qabiliyyəti azaldıla, kəsilə, çevrilə, fırladıla bilər və kafel strukturu faylın tam dekodlanması olmadan dəyişdirilə bilər.
- **Metaməlumat Dəstəyi**: JPEG XR şəkil faylı çoxsaylı cihazlarda ardıcıl rəng təmsili üçün ICC rəng profilindən ibarət ola bilər. Format Exif və XMP metadata formatlarını da dəstəkləyir.

## Konteyner Format ##

JPEG XR təsvir məlumatları Şəkil Fayl Kataloqunun (IFT) teqləri cədvəlindən istifadə etməklə TIFF kimi konteyner formatında saxlanıla bilər. JXR faylı IFD teqlərində aşağıdakıları ehtiva edir:

- Şəkil məlumatı: Bu, bitişik öz-özünə əhatə olunan şəkil məlumatıdır.
- İsteğe bağlı alfa kanalı məlumatları: Əgər bu varsa, şəffaflığı dəstəkləməyən tətbiqləri dəstəkləmək üçün təsvir məlumatları ayrıca sıxıla bilər.
- Metadata
- Könüllü XMP metadata
- Könüllü Exif metadata

TIFF formatına əsaslandığı üçün 4 GB fayl ölçüsü limiti kimi bütün TIFF format məhdudiyyətlərini miras alır.

## İstinadlar ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

