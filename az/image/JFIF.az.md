---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF faylı - .jfif fil nədire?
linktitle: JFIF
description: LJFIF fayl formatı və JFIF faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## JFIF faylı nədir?

JFIF (JPEG Fayl Mübadilə Formatı (JFIF)) .jfif uzantısından istifadə edən şəkil formatı faylıdır. JFIF mürəkkəbliyi azaltmaqla və onun məhdudiyyətlərini həll etməklə JIF (JPEG Mübadilə Formatı) üzərində qurur.

## JFIF-in qısa tarixi

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. 1.02 versiyası 7 sentyabr 1992-ci ildə nəşr olundu. RFC 2046 JFIF formatının JPEG şəkillərini internet üzərindən ötürmək üçün istifadə edildiyini qeyd etdi. JFIF 2009-cu ildə ECMA tərəfindən nəşr edilib və 2011-ci ildə T.871 Tövsiyəsi kimi ITU-T tərəfindən və 2013-cü ildə ISO/IEC tərəfindən ISO/IEC 10918-5 kimi standartlaşdırılıb.

## JFIF Fayl Format ##

JFIF faylı JPEG Standartının 1-ci hissəsində müəyyən edilmiş markerlər ardıcıllığından ibarətdir. Hər bir marker iki baytdan ibarətdir (FF və ardınca markerin növünü göstərən bayt). Markerlər ya müstəqil ola bilər, ya da marker seqmentinin başlanğıcını göstərə bilər.

JFIF, Y, Cb, Cr kimi bir çox komponentin fərqli qətnamələrə malik olmasına imkan verir, lakin onların düzülüşü müəyyən edilmir. JPEG-dən fərqli olaraq, JFIF qətnamə və aspekt nisbəti haqqında məlumat verə bilər. JFIF həmçinin istifadə olunacaq rəng modelini də müəyyən edir.

### Fayl strukturu ##

|Seqment|Kod|Təsvir|
|---|---|---|
|SOI|FF D8|Şəkilin başlanğıcı|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|əlavə marker seqmentləri|
|SOS|FF DA|Skanın Başlanması|
||sıxılmış şəkil verilənləri||
|EOI|FF D9|Şəkilin sonu|

JFIF Standartı aşağıdakı seqmentləri müəyyən edir:

### JFIF APP0 marker seqmenti ###

Şəkil parametrlərini ehtiva edən məcburi bir seqmentdir. O, həmçinin daxil edilmiş sıxılmamış miniatürdən ibarət ola bilər.

|Sahə|Ölçü (bayt)|Təsvir|
|---|---|---|
|APP0 marker|2|FF E0|
|Uzunluq|2|APP0 markeri istisna olmaqla seqmentin uzunluğu|
|İdentifikator|5|Nul baytla dayandırılmış ASCII-də JFIF (4A 46 49 46 00)|
|JFIF versiyası|2|JFIF versiyası|
|Sıxlıq vahidləri|1|Aşağıdakı piksel sıxlığı sahələri üçün vahid</br> 00 : Vahid yoxdur; width:height piksel aspekt nisbəti Ydensity:Xdensity ilə bərabərdir</br> 01 : Düym başına piksel</br> 02 : Santimetrdə piksel|
|Xdensity|2|Üfüqi piksel sıxlığı sıfırdan böyük|
|Ydensity|2|Sıfırdan böyük şaquli piksel sıxlığı|
|Xthumbnail|1|Daxil edilmiş RGB miniatürünün üfüqi piksel sayı. Sıfır ola bilər|
|Ythumbnail|1|Daxil edilmiş RGB miniatürünün şaquli piksel sayı. Sıfır ola bilər|
|Minimal data|3 × n|sıxılmamış 24 bit RGB raster miniatür datası|

### JFIF genişləndirilməsi APP0 marker seqmenti ###

Bu, müəyyən edilərsə, dərhal JFIF APP0 marker seqmentini izləməli olan isteğe bağlı bölmədir. Bu bölmə JFIF 1.02 və yuxarı versiyaları tərəfindən dəstəklənir və üç müxtəlif formatda miniatürlərin daxil edilməsinə imkan verir.

|Sahə|Ölçü (bayt)|Təsvir|
|---|---|---|
|APP0 marker|2|FF E0|
|Uzunluq|2|APP0 markeri istisna olmaqla seqmentin uzunluğu|
|İdentifikator|5|ASCII-də JFXX (4A 46 58 58 00) null baytla dayandırılıb|
|Thumbnail format|1|Aşağıdakı daxil edilmiş miniatür üçün hansı məlumat formatının istifadə olunduğunu müəyyən edir:</br> 10 : JPEG formatı</br> 11: 1 bayt hər piksel üçün paletləşdirilmiş format</br> 13 : piksel başına 3 bayt RGB formatı|
|Minimal data|dəyişən||

## JFIF-in Digər Şəkil Fayl Formatlarına çevrilməsi

JFIF [PNG](/image/png/), [JPG](/image/jpeg/) və [PDF](/pdf/) kimi məşhur şəkil fayl formatlarına çevrilə bilər.

## İstinadlar ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

