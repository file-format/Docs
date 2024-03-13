---
date: 2021-03-21
keywords: alac, alac file format, .alac extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LALAC fayl formatı və ALAC faylını yarada və aça bilən API-lər haqqında qazanıns.
title: ALAC - Apple Lossless Audio Codec Fayl Formasıat
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## ALAC faylı nədir?

ALAC fayl formatı MPEG-4 uyğun QuickTime konteynerindən istifadə edən Apple Lossless Audio Codec-dir (ALAC). O, 2004-cü ildə xüsusi fayl formatı kimi təqdim edildi, 2011-ci ilə qədər Apple onu açıq mənbə və royaltisiz təqdim edənə qədər. Format [FLAC](/audio/flac/) (Free Lossless Audio Codec) ilə oxşardır, lakin nisbətən daha çox sıxılma təklif edir. O, [AAC](/audio/aac/) və ya [MP3](/audio/mp3/) üçün daha yaxşı səsli alternativ təklif edir. ALAC kodek ilə kodlanmış audio faylları Apple QuickTime, Apple iTunes və K-Lite kodekli Micrsoft Windows Media Player istifadə edərək açmaq olar.

## ALAC fayl formatı

ALAC kodekinə əsaslanan fayllar tərtibatçının istinadı üçün [open source on GitHub](https://github.com/macosforge/alac) kimi əlçatan olan ikili fayllardır. O, ALAC kodlayıcı və dekoder üçün mənbələri ehtiva edir. Apple həmçinin Core Audio Format (CAF) və [WAVE](/audio/wav/) fayllarına audio verilənləri oxumaq və yazmaq üçün `alacconvert` adlı komanda xətti yardım proqramını təqdim etmişdir. Aşağıda ALAC fayl formatı ilə bağlı bəzi əsas məqamlar verilmişdir.

 1. `Bit Dərinlikləri` - 16, 20, 24 və 32 bit.
 1. `Sample Rate` - 1-dən 384.000 Hz-ə qədər istənilən ixtiyari tam ədəd seçmə tezliyi. 4,294,967,295 (2^32 - 1) Hz-ə qədər nəzəri sürətlər dəstəklənə bilər.
 1. `Paket Ölçüsü` - Defolt paket ölçüsü paket başına səsin 4096 nümunə çərçivəsidir. Digər paket ölçüləri, şübhəsiz ki, mümkündür. Bununla belə, standart olmayan paket ölçülərinin Apple Lossless-i dəstəkləyən bütün aparat cihazlarında düzgün işləməsinə zəmanət verilmir. 16.384 nümunə çərçivədən yuxarı paketlər dəstəklənmir.
 1. `Dəstəklənən Kanallar` - Birdən səkkizədək kanalı dəstəkləyir. Hər bir kanal aşağıdakı məlumat sırasına malikdir.

|Num Chan| Sifariş |
|---|---|
|1 |mono|
|2 |stereo (Sol, Sağ)|
|3 |MPEG 3.0 B (Mərkəz, Sol, Sağ)|
|4 |MPEG 4.0 B (Mərkəz, Sol, Sağ, Mərkəz Ətrafı)|
|5 |MPEG 5.0 D (Mərkəz, Sol, Sağ, Sol Ətraf, Sağ Ətraf)|
|6 |MPEG 5.1 D (Mərkəz, Sol, Sağ, Sol Ətraf, Sağ Ətraf, Aşağı Tezlik Effektləri)|
|7 |Apple AAC 6.1 (Mərkəz, Sol, Sağ, Sol Ətraf, Sağ Ətraf, Mərkəz Ətraf, Aşağı Tezlik Effektləri)|
|8 |MPEG 7.1 B (Mərkəz, Sol Mərkəz, Sağ Mərkəz, Sol, Sağ, Sol Ətraf, Sağ Ətraf, Aşağı Tezlik Effektləri)|

## İstinadlar

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)

* [Apple Lossless Audio Codec](https://macosforge.github.io/alac/)

* [macosforge - GitHub-da alac](https://github.com/macosforge/alac)


