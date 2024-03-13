---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF fayl formasıat
linktitle: FLIF
description: LFLIF fayl formatı və FLIF faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## FLIF faylı nədir? ##

FLIF (Free Lossless Image Format) faylları üçün .flif uzantısından istifadə edən itkisiz şəkil formatıdır. FLIF sıxılma nisbətinə görə [PNG](/image/png/), itkisiz [WebP](/image/webp/), itkisiz BPG və itkisiz JPEG 2000-dən üstün olduğunu iddia edir. FLIF mütərəqqi interlacing-dən istifadə edir, buna görə şəklin istənilən qismən endirilməsi bütün təsvir üçün itkili kodlaşdırma kimi istifadə edilə bilər.

## Qısa tarix ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. 2016-cı ilin sentyabrında FLIF-in ilk stabil versiyası buraxıldı.

## FLIF Dizayn ##

FLIF sıxılma üçün CABAC (Context-adaptive binar arifmetic coding), MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) variantından istifadə edir. MANIAC Jon Sneyers və Pieter Wuille tərəfindən hazırlanmış entropiya kodlaşdırma alqoritmidir. MANIAC-da kontekstlər dinamik kodlaşdırma zamanı öyrənilən qərar ağaclarının qovşaqlarıdır. Bu, kontekst modelini daha çox təsvirə xas edir və daha yaxşı sıxılma ilə nəticələnir. FLIF aşağıdakı xüsusiyyətlərə malikdir:

- İtkisiz sıxılmanı dəstəkləyir
- Kodlayıcının əvvəlcədən işlənməsi ilə itkili sıxılmanı dəstəkləyir
- Greyscale, RGB və RGBA dəstəkləyir
- Kanal başına 1 ilə 16 bit rəng dərinliyini dəstəkləyir
- İnterlaced və qeyri-interlaced faylları dəstəkləyir
- Qismən yüklənmiş faylların mütərəqqi dekodlanmasını dəstəkləyir
- Animasiyalar dəstəkləyir
- Daxili ICC rəng profillərini, Exif və XMP metadatasını dəstəkləyir
- Kamera xam fayllarını sıxmaq üçün məhdud dəstəyə malikdir (RGGB)

## FLIF Fayl Formatı ##

FLIF faylı aşağıdakı dörd hissədən ibarətdir:

## Əsas başlıq ##

Əsas başlıq genişlik, hündürlük, rəng dərinliyi, çərçivələrin sayı daxil olmaqla əsas metadatadan ibarətdir.

|Növ|Dəyər|Təsvir|
|---|---|---|
|4 bayt|FLIF|Sehrli|
|4 bit|3 = ni still; 4 = mən hələ də; 5 = ni anim; 6 = i anim|Bir-birinə keçid, animasiya|
|4 bit|1 = Boz rəng; 3 = RGB; 4 = RGBA|Kanalların sayı (nb_channels)|
|1 bayt|'0','1','2' ('0'=xüsusi)|Kanal başına bayt (Bpc)|
|varint|en-1|Eni|
|varint|hündürlük-1|Hündürlük|
|varint|nb_frames-2 (yalnız animasiya olduqda)|Kadrların sayı (nb_frames)|

## Metadata parçaları ##

Bu hissə Exif/XMP metadatası, ICC rəng profili və s. kimi qeyri-pikselləri ehtiva edir və DEFLATE sıxılma ilə kodlanır. Bu hissələr PNG parçaları ilə eyni şəkildə müəyyən edilir, fərq, çubuq ölçüsünün dəyişən bayt sayı ilə kodlanmasıdır. Parçaların adları 4 hərf (4 bayt) və ya 32-dən aşağı dəyər ola bilər ki, bu da isteğe bağlı olmayan yığını göstərir.

Aşağıda isteğe bağlı çəngəllərin nümunəsi verilmişdir:

|Bölmə adı|Təsvir|Məzmun (DEFLATE-dekompressiyadan sonra)|
|---|---|---|
|iCCP|ICC rəng profili|xam ICC rəng profili datası|
|eXif|Exif metadata|Exif\0\0 başlığı, ardınca TIFF başlığı və EXIF datası|
|eXmp|XMP metadata|XMP doldurulması olmayan yalnız oxuna bilən xpacket daxilindədir|

### Ad Konvensiyası ###

- **İlk hərf**: Böyük hərf kritik, kiçik hərf isə qeyri-kritik parçalar üçün istifadə olunur.
- **İkinci Hərf**: Böyük hərf ictimai, kiçik hərf isə şəxsi parçalar üçün istifadə olunur
- **Üçüncü Hərf**: Şəkli düzgün göstərmək üçün lazım olan böyük hərflər üçün istifadə olunur və şəkli göstərmək üçün kiçik hərf vacib deyil.
- **Dördüncü Hərf**: Böyük hərf kor-koranə şəkildə kopyalana bilən çubuqlar üçün istifadə olunur. Kiçik hərflər şəkil məlumatlarından asılıdır.

## İkinci başlıq ##

Bu, piksellərin faktiki kodlaşdırılması ilə bağlı məlumatları ehtiva edir.

|Növ|Təsvir|Şərt|Defolt dəyər|
|---|---|---|---|
|1 bayt|NUL bayt (0x00), FLIF16 bit axınının yığın adı||
|uni_int(1,16)|Kanalların piksel başına bit|Bpc == '0': təkrar(nb_channels)|8 əgər Bpc == '1', 16 əgər Bpc == '2'|
|uni_int(0,1)|Bayraq: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Dövrələrin sayı|nb_çərçivə > 1||
|uni_int(0,60_000)|ms-də çərçivə gecikməsi|nb_frames > 1: təkrar(nb_frames)|
|uni_int(0,1)|Bayraq: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|kəsmə|xüsusi_kesmə_və_alfa|2|
|uni_int(2,128)|alfa bölücü|xüsusi_cutoff_and_alpha|19|
|uni_int(0,1)|Bayraq: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|xüsusi_bitchance||
|dəyişən|Transformasiyalar (aşağıya bax)|||
|uni_int(1) = 0|Göstərici bit: çevrilmələrlə tamamlandı|||
|uni_int(0,2)|Görünməz piksel proqnozlaşdırıcısı|alpha_zero && interlaced && alfa diapazonuna sıfır daxildir||

**Kanallar**

|Kanal nömrəsi|Təsvir|
|---|----|
|0|Qırmızı və ya Boz|
|1|Yaşıl|
|2|Mavi|
|3|Alfa|

**Çevrilmələr**

|Növ|Təsvir|
|---|---|
|uni_int(1) = 1|Göstərici bit: hələ tamamlanmayıb|
|uni_int(0,13)|Transformasiya identifikatoru|
|dəyişən|Transformasiya məlumatları (transformasiyadan asılıdır)|

Transformasiya daha yaxşı sıxılma üçün piksel məlumatlarını dəyişdirmək və əslində baş verən piksel dəyərlərini izləmək üçün istifadə olunur.

## Piksel Data ##

Bu hissə MANIAC entropiya kodlaşdırmasından istifadə edərək kodlanmış faktiki piksel məlumatlarını ehtiva edir. Piksellər interlaced və ya qeyri-interlaced kodlaşdırma ilə kodlaşdırıla bilər.

### Keçidilmiş üsul ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Başqa sözlə, hər cüt nömrəli böyütmə səviyyəsi 2k təsvirin 1:2^k miqyasında aşağı nümunəli versiyasıdır. Böyütmə səviyyələri ən yüksəkdən ən aşağıya doğru kodlanır.

### Bir-birinə qarışmayan üsul ###

Bu üsulda MANIAC ağaclarının kodlaşdırılması dərhal piksellərin kodlaşdırılması ilə başlayır.

## İstinadlar ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

