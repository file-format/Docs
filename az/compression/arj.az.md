---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ fayl formasıat
linktitle: ARJ
description: LARJ fayl formatı və ARJ faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## ARJ faylı nədir? ##

ARJ (Robert Jung tərəfindən arxivləşdirilmiş) Robert K. Jung tərəfindən hazırlanmış yüksək səmərəli sıxılmış arxiv faylıdır. ARJ 1990-cı illərin əvvəllərində DOS və Windows-un erkən versiyaları üçün hazırlanmışdır. ARJ faylları çox sayda faylın ehtiyat nüsxəsini çıxarmaq və ya paylaşmaq üçün faydalıdır, çünki bütün bu faylları izləmək məcburiyyətində deyilsiniz və idarə etmək üçün yalnız bir fayl var. .arj uzantısı ARJ arxiv faylları üçün istifadə olunur.

## ARJ Fayl Formatı ##

ARJ faylı iki növ başlıqdan ibarətdir:

- Əsas başlıq: Arxivin əvvəlində bir əsas başlıq var.
- Yerli başlıqlar: Yerli başlıqlar hər fayldan əvvəl mövcuddur.

|Offset|Növ|Sayı|Təsvir|
|---|---|---|---|
|0000h|söz|1|ID=0EA60h|
|0002h|söz|1|əsas başlıq ölçüsü|
|0004h|bayt|1|Başlığın ölçüsü|
|0005h|bayt|1|Arxiv versiya nömrəsi|
|0006h|bayt|1|Minimum versiya nömrəsi lazımdır|
|0007h|bayt|1|Host OS:</br> 0 - MS-DOS</br> 1 - PRİMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Sistem xx)</br> 5 - ƏS/2</br> 6 - APPLE GS</br> 7 - ATARI ST</br> 8 - Sonrakı</br> 9 - VAX VMS|
|0008h|bayt|1|Daxili Bayraqlar, bitmaplanmış:</br> 0 - parol / parol yoxdur</br> 1 - qorunur</br> 2 - fayl növbəti diskdə davam edir</br> 3 - faylın başlanğıc mövqeyi sahəsi mövcuddur</br> 4 - yolun tərcüməsi ( \ - / )|
|0009h|bayt|1|Sıxılma üsulu:</br> 0 - saxlanılır</br> 1 - ən çox sıxılmışdır</br> 2 - sıxılmış</br> 3 - daha sürətli sıxılır</br> 4 - ən sürətli sıxılmış|
|000Ah|bayt|1|Fayl növü:</br> 0 - ikili</br> 1 - 7 bitlik mətn</br> 2 - şərh başlığı</br> 3 - kataloq</br> 4 - həcm etiketi|
|000Bh|bayt|1|ehtiyatda|
|000Ch|dword|1|MS-DOS formatında orijinal faylın Tarixi/Vaxtı|
|0010h|dword|1|Sıxılmış faylın ölçüsü|
|0014h|dword|1|Orijinal faylın ölçüsü|
|0018h|dword|1|Orijinal faylın CRC-32|
|001Ah|söz|1|Fayl adında fayl xüsusiyyətlərinin mövqeyi|
|001Ch|söz|1|Fayl atributları|
|001Eh|söz|1|Host məlumatı|
|?|dword|1|Genişləndirilmiş faylın başlanğıc mövqeyi|
|????h|dword|1|Əsas başlığın CRC-32|
|????h|söz|1|İlk genişləndirilmiş başlığın ölçüsü|
|????h+SIZ+2|dword|1|Genişləndirilmiş başlığın CRC-32|
|????h+SIZ+6|bayt|?|Sıxılmış fayl|

## İstinadlar ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

