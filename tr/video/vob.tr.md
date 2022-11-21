---
date: 2019-10-11
keywords: vob, .vob, vob dosya biçimi, .vob dosya biçimi, .vob uzantısı, vob uzantısı, vob video biçimi, vob dvd dosyaları
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "VOB dosya formatı ve VOB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: VOB Dosya Biçimi
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## VOB dosyası nedir? ##

VOB dosyaları tipik olarak .vob uzantılı bir DVD'deki VIDEO_TS dizininde saklanır. VOB dosyaları, video ve ses verilerinin yanı sıra menüler ve altyazılar gibi diğer verileri içerir. VOB, MPEG-2 program akışı biçimini temel alır, ancak özel akışlarda ek sınırlamaları ve özellikleri vardır. VOB dosyaları, MPEG program akışlarının katı bir alt kümesidir, dolayısıyla tüm VOB dosyaları MPEG program akışlarıdır ancak tüm MPEG program akışları, VOB uyumlu değildir.

## DVD Video Yapısı ##

Bir bilgisayarda bir DVD açıldığında, VIDEO_TS, AUDIO_TS ile en üst düzey dizindir. AUDIO_TS boştur ve kullanılmaz. VIDEO_TS dizini içerisinde VOB, BUP ve IFO dosyaları bulunmaktadır. VOB dosyaları MPEG içeriğini içerir. Bunlar, tüm işletim sistemleriyle uyumlu olacak şekilde 1 GB veya daha küçük boyutlu parçalara bölünür. IFO dosyaları, menüler ve başlık yapısı ile ilgili bilgiler içerir. BUK dosyaları, aynı ada sahip IFO dosyalarının yedek dosyalarıdır. Bu dosyaların fiziksel olarak ayrı bir alanda tutulması amaçlanmıştır, böylece DVD'deki fiziksel hasar nedeniyle IFO dosyasının hasar görmesi durumunda BUK dosyası aynı bilgileri sağlayabilir.

### Fiziksel Düzen ###

- Diskteki tüm dosyalar bitişik olmalıdır.
- İlgili dosyalar yan yana (VOB, IFO, BUP) olmalıdır.
- Numaralandırılmış dosyalar artan sırada olmalıdır.

## Kopya Koruma ##

Birçok video DVD'si şifrelidir ve DVD'den veri kopyalanmasını engeller. DVD'nin erişilemeyen giriş alanında bulunan dosyaları oynatmak için kimlik doğrulama ve şifre çözme anahtarlarına ihtiyaç vardır. Bu anahtarlar, DVD oynatıcıda veya yazılım oynatıcıda bulunan CSS şifre çözme yazılımı tarafından kullanılır. Anahtarlar olmadan, dosyalar açıldığında anahtarlar isteneceğinden video dosyaları oynatılamaz.

## Referanslar ##

- [VOB - Vikipedi](https://en.wikipedia.org/wiki/VOB)
- [İç DVD-Video/Directory Yapısı](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

