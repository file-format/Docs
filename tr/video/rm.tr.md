---
date: 2019-10-11
keywords: rm, .rm, rm dosya biçimi, .rm dosya biçimi, .rm uzantısı, RealMedia dosya biçimi
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RM dosya formatı ve RM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: RM Dosya Biçimi
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## RM dosyası nedir? ##

RealMedia, RealNetworks tarafından geliştirilen ve .rm uzantısını kullanan tescilli bir multimedya kapsayıcı biçimidir. İnternet üzerinden akış için [RealAudio (RA)](/tr/audio/ra/) ve [RealVideo(RV)](/tr/video/rv/) kombinasyonu ile kullanılır. Bu akışlar sabit bit hızındadır. RealNetworks, değişken bit hızı için RealMedia Değişken Bit Hızı (RMVB) formatını geliştirdi. RealMedia, internet üzerinden içerik akışı için uygundur ve örneğin canlı televizyon akışı için kullanılabilir.

## RealMedia Dosyasının Yapısı ##

Bir RealMedia dosyası, her biri aşağıdaki yapıya sahip bir dizi parçadan oluşur:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

RealMedia dosyasında bulunan parça türleri şunlardır:

- **RealMedia dosya başlığı (.RMF)**: Bu, RealMedia dosyasındaki ilk parça olmalıdır. Bir dosyada yalnızca bir RMF öbeği bulunur. Başlık sayısı hakkında bilgi içerir.
- **Dosya özellikleri başlığı (PROP)**: Bu, RealMedia dosyasının genel özellikleri hakkında bilgi içerir. Her RealMedia dosyasında bu türden yalnızca bir öbek vardır.
- **Medya özellikleri başlığı (MDPR)**: Bu yığın, akış özellikleri hakkında bilgi içerir. Akış türü ve kullanılan codec bileşeni hakkında bilgi içerir. Dosyadaki her akış için bir MDPR öbeği vardır.
- **İçerik açıklama başlığı (CONT)**: Bu parça, RealMedia dosyasındaki içeriğin başlığı veya yazarı gibi metin bilgilerini içerir. Bu yığın sadece bilgi amaçlıdır.
- **Veri başlığı (DATA)**: Bu parça, bir grup veri paketi içerir.
- **Dizin başlığı (INDX)**: Bu parça, tüm DATA parçalarından sonra gelir ve dizin girişlerini içerir. Bir dosya birden fazla INDX parçasına sahip olabilir.

## Desteklenen ses ve video formatları ##

### Ses biçimleri ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- siper: Sipro
- aşçı: Aşçı
-atrc: ATRAC3
- ralf: RealAudio Kayıpsız Biçimi
- raac: LC-AAC
- rakp: HE-AAC

### Video biçimleri ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 öncüsü
- RV40: H.264 öncüsü, RV40
- RVTR: H.263+ (RV20)

## Referanslar ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

