---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LRM fayl formatı və RM faylı yarada və aça bilən API-lər haqqında qazanıns.
title: RM fayl formasıat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## RM faylı nədir? ##

RealMedia, .rm genişlənməsindən istifadə edən RealNetworks tərəfindən hazırlanmış xüsusi multimedia konteyner formatıdır. İnternet üzərindən yayım üçün [RealAudio (RA)](/audio/ra/) və [RealVideo(RV)](/video/rv/) kombinasiyası ilə istifadə olunur. Bu axınlar sabit bit sürətinə malikdir. Dəyişən bit sürəti üçün RealNetworks RealMedia Dəyişən Bitrate (RMVB) formatını işləyib hazırlayıb. RealMedia internet üzərindən məzmun axını üçün uyğundur və məsələn, canlı televiziya yayımı üçün istifadə edilə bilər.

## RealMedia Faylının Strukturu ##

RealMedia faylı hər biri aşağıdakı struktura malik olan bir sıra hissələrdən ibarətdir:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

RealMedia faylında mövcud olan hissələrin növləri aşağıdakılardır:

- **RealMedia fayl başlığı (.RMF)**: Bu, RealMedia faylında ilk hissə olmalıdır. Bir faylda yalnız bir RMF yığını mövcuddur. Başlıqların sayı haqqında məlumat ehtiva edir.
- **Fayl xassələri başlığı (PROP)**: Bu, RealMedia faylının ümumi xüsusiyyətləri haqqında məlumatı ehtiva edir. Hər RealMedia faylında bu tipdən yalnız bir parça var.
- **Media xassələri başlığı (MDPR)**: Bu hissədə axın xüsusiyyətləri haqqında məlumat var. Burada axın növü və istifadə olunan kodek haqqında məlumat var. Faylda hər axın üçün bir MDPR yığını var.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **Məlumat başlığı (DATA)**: Bu hissə bir qrup məlumat paketini ehtiva edir.
- **İndeks başlığı (INDX)**: Bu hissə bütün DATA parçalarından sonra gəlir və indeks qeydlərini ehtiva edir. Bir faylda birdən çox INDX parçası ola bilər.

## Dəstəklənən audio və video formatları ##

### Audio formatlar ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- şəbəkə: AC3
- sipr: Sipro
- aşpaz: bişir
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Video formatları ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 prekursoru
- RV40: H.264 prekursoru, RV40
- RVTR: H.263+ (RV20)

## İstinadlar ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

