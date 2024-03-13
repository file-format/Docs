---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LFLV fayl formatı və FLV faylını yarada və aça bilən API-lər haqqında qazanıns.
title: FLV Fayl Formasıat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## FLV faylı nədir? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe sistemləri FLV məhdudiyyətlərinə görə 2007-ci ildə F4V-ni yaratdı.

### Kodlaşdırma ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. On2 TrueMotion VP6 video bit axını üçün Flash Player-in 8-ci versiyası. Flash Player 8 və daha yüksək versiyalar üçün tövsiyə olunan sıxılma formatıdır. FLV MP3-də audio, Nellymoser Asao Codec və açıq mənbəli Speex kodekini dəstəkləyir. O, həmçinin sıxılmamış audio və ya ADPCM formatlı audionu dəstəkləyir. AAC (HE-AAC/AAC SBR, AAC Əsas Profili və AAC-LC) Flash Player 9-un son versiyaları tərəfindən dəstəklənir.

## Struktur ##

FLV faylları Başlıq və Paketlərdən ibarətdir. FLV faylı Başlıqdan başlayır. Başlıqda aşağıdakı sahələr var.

- **İmza**: Onun dəyəri FLV-dir
- **Version**: Its default value is 1. Yalnız 0x01 etibarlıdır.
- **Bayraqlar**: 0x04 audio üçün, 0x01 isə video üçün istifadə olunur, buna görə də 0x05 həm audio, həm də video üçün istifadə olunur.
- **Header Size**: The default value is 9. Daha yeni genişləndirilmiş başlığı keçmək üçün istifadə olunur.

Başlıqdan sonra Paketlər gəlir. FLV faylı 15 baytlıq başlıqları olan FLV teqləri adlanan çoxsaylı paketlərə bölünür. Paketlərdə audio, video, skriptlər, şifrələmə məlumatı və faydalı yük üçün metadata var. FLV paketlərində aşağıdakı sahələr var.

- **Reserved**: FMS üçün qorunur və 0 olmalıdır.
- **Filtr**: Paketlərin süzülüb-süzülmədiyini göstərir.
  - "**0**: Əvvəlcədən emal tələb olunmur. Bu şifrələnməmiş fayllar üçün istifadə olunur."
  - "**1**: Əvvəlcədən emal tələb olunur. Bu şifrələnmiş fayllar üçün istifadə olunur"
- **Paket Tipi**: Bu, paketdəki məzmunun növünü müəyyən edir.
  - "**8**: Audio"
  - "**9**: Video"
  - "**18**: Skript Məlumatı"
- **Məlumat Ölçüsü**: Bu mesajın uzunluğunu bildirir.
- **Timstamp Lower**: Bu, etiket məlumatının tətbiq olunduğu vaxt damgasını millisaniyələrdə saxlayır. İlk paket üçün NULL olaraq təyin edilmişdir.
- **Yuxarı Zaman damğası**: uint32_be dəyəri yaratmaq üçün genişləndirmə.
- **Stream ID**: Bu, ilk axın üçün NULL olaraq təyin edilib.
- **Payload Data**: Bu, paket növünə əsaslanan məlumatdır.

## İstinadlar ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

