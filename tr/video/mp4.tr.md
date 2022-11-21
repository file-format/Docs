---
date: 2019-10-11
keywords: MP4, dosya, uzantı, format, video formatı, MPEG-4
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "MP4 dosya biçimi ve MP4 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: MP4 Dosya Biçimi
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## MP4 dosyası nedir? ##

MP4 (MPEG-4 Kısım 14'ün kısaltması), ISO/IEC 14496-12:2004'e dayalı, QuickTime Dosya Formatına dayalı, ancak İlk Nesne Tanımlayıcıları (IOD) ve diğer MPEG özelliklerini resmi olarak desteklediğini belirten bir dosya formatıdır. Çoğunlukla video ve ses depolamak için kullanılır, ancak altyazıları ve hareketsiz görüntüleri depolamak için de kullanılabilir. MP4 dosyaları .mp4 uzantısıyla saklanır. MP4, uluslararası bir görsel-işitsel kodlama standardıdır. Çoğu modern konteyner formatına benzer şekilde, MP4 internet üzerinden akışı destekler. MP4'te kullanılan yüksek sıkıştırma nedeniyle, ortaya çıkan dosyaların boyutu daha küçüktür ve neredeyse tüm orijinal kalite korunur.

## Kısa Tarih ##

MP4 özelliği, Moving Picture Experts Group (MPEG) tarafından geliştirilmiştir ve 2001'de yayınlanan QuickTime biçimine [MOV](/tr/video/mov/) dayanmaktadır. MP4'ün ilk sürümü (ISO/IEC 14496-1:2001) 1999'da yayınlanan MPEG-4 Bölüm 1: Sistem spesifikasyonunun bir revizyonuydu. MP4 dosya formatı, zamana dayalı medya dosyalarının genel yapısını tanımlayan ISO Temel Medya Dosyası Formatı ISO/IEC 14496-12:2004'e genelleştirildi. Sonuç olarak, diğer dosya biçimleri için bir temel olarak kullanılır.

## MP4 Dosyalarının Yapısı ##

MP4, genişletilebilir bir kapsayıcı dosyasıdır, yani katı bir yapı tanımlamaz ve her ortam türü için özel yapı ve hiyerarşiye izin verir. MP4 dosyasındaki veriler, birincisi ortamla ilgili verileri ve ikincisi meta verileri içeren iki bölüme ayrılmıştır. Medya verileri ses veya video içerir ve meta veriler rasgele erişim, zaman damgaları vb.
MP4'teki yapılar tipik olarak atomlar veya kutular olarak adlandırılır. Bir atomun minimum boyutu 8 bayttır (ilk 4 bayt boyutu belirtir ve sonraki 4 bayt türü belirtir). MP dosyalarında bulunan kök düzeyindeki atomların bir listesi:

- **ftyp**: Dosya türünü, açıklamasını ve kullanılan ortak veri yapılarını içerir.
- **pdin**: Aşamalı video yükleme/indirme bilgilerini içerir.
- **moov**: Tüm film meta verileri için kapsayıcı.
- **moof**: Video parçaları içeren kapsayıcı.
- **mfra**: Video parçasına rastgele erişime sahip kapsayıcı
- **mdat**: Medya için veri kabı.
- **stts**: örnekten zamana tablo.
- **stsc**: örnekten yığına tablo.
- **stsz**: örnek boyutları (çerçeveleme)
- **meta**: Meta veri bilgilerinin bulunduğu kapsayıcı.

İşte MP4'te kullanılan ikinci seviye atomların bir listesi:

- **mvhd**: Videonun tüm ayrıntılarını içeren video başlık bilgilerini içerir.
- **trak**: Bireysel raylı konteyner.
- **udta**: Kullanıcı ve parça bilgilerini içeren kapsayıcı.
- **iods**: MP4 dosya tanıtıcısı

## Referanslar ##

- [MP4 - Vikipedi](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

