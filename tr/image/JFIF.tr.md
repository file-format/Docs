---
date: 2020-08-12
keywords: jfif, .jfif, jfif dosya formatı, jfif dosyaları nasıl açılır, .jfif uzantısı, jfif uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF Dosyası - .jfif dosyası nedir?
linktitle: JFIF
description: "JFIF dosya formatı ve JFIF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## JFIF dosyası nedir?

JFIF (JPEG File Interchange Format (JFIF)) .jfif uzantısını kullanan bir resim formatı dosyasıdır. JFIF, karmaşıklığı azaltarak ve sınırlamalarını çözerek JIF (JPEG Değişim Formatı) üzerine kuruludur.

## JFIF'in Kısa Tarihi

JFIF belge geliştirmesi Eric Hamilton tarafından yönetildi ve 1991'in sonlarında ilk sürüm için bir anlaşma yapıldı. Sürüm 1.02, 7 Eylül 1992'de yayınlandı. RFC 2046, JFIF formatının internet üzerinden JPEG görüntüleri iletmek için kullanıldığını belirtti. JFIF, ECMA tarafından 2009 yılında yayınlandı ve ITU-T tarafından 2011 yılında Tavsiye T.871 olarak ve ISO/IEC tarafından 2013 yılında ISO/IEC 10918-5 olarak standardize edildi.

## JFIF Dosya Biçimi ##

Bir JFIF dosyası, JPEG Standardının 1. bölümünde tanımlandığı gibi bir dizi işaretçiden oluşur. Her işaretçi iki bayttan oluşur (FF ve ardından işaretçinin türünü belirten bir bayt). İşaretçiler bağımsız olabilir veya bir işaretçi segmentinin başlangıcını gösterebilir.

JFIF, Y, Cb, Cr gibi birden çok bileşenin farklı çözünürlüklere sahip olmasına izin verir, ancak hizalamaları tanımlanmamıştır. JPEG'den farklı olarak JFIF, çözünürlük ve en boy oranı bilgisi sağlayabilir. JFIF ayrıca kullanılacak renk modelini de tanımlar.

### Dosya Yapısı ##

|Segment|Kod|Açıklama|
|---|---|---|
|SOI|FF D8|Görüntünün Başlangıcı|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|ek işaret segmentleri|
|SOS|FF DA|Taramanın Başlangıcı|
||sıkıştırılmış görüntü verileri||
|EOI|FF D9|Görüntünün Sonu|

JFIF Standardı aşağıdaki segmentleri tanımlar:

### JFIF APP0 işaretçi segmenti ###

Görüntü parametrelerini içeren zorunlu bir bölümdür. Ayrıca gömülü, sıkıştırılmamış bir küçük resim içerebilir.

|Alan|Boyut (bayt)|Açıklama|
|---|---|---|
|APP0 işaretçisi|2|FF E0|
|Uzunluk|2|APP0 işaretçisi hariç segmentin uzunluğu|
|Tanımlayıcı|5|ASCII'deki JFIF (4A 46 49 46 00) boş bayt tarafından sonlandırıldı|
|JFIF versiyonu|2|JFIF versiyonu|
|Yoğunluk birimleri|1|Aşağıdaki piksel yoğunluğu alanları için birim</br> 00 : Birim yok; genişlik:yükseklik piksel en boy oranı, Ydensity:Xdensity'ye eşittir</br> 01 : Piksel/inç</br> 02 : Piksel/santimetre|
|Xdensity|2|Yatay piksel yoğunluğu sıfırdan büyük|
|Ydensity|2|Dikey piksel yoğunluğu sıfırdan büyük|
|Xthumbnail|1|Gömülü RGB küçük resminin yatay piksel sayısı. sıfır olabilir |
|Ythumbnail|1|Gömülü RGB küçük resminin dikey piksel sayısı. sıfır olabilir |
|Küçük resim verileri|3 × n|Sıkıştırılmamış 24 bit RGB raster küçük resim verileri|

### JFIF uzantısı APP0 işaretçi segmenti ###

Bu, tanımlandığı takdirde JFIF APP0 işaretleyici segmentini hemen takip etmesi gereken isteğe bağlı bir bölümdür. Bu bölüm, JFIF sürüm 1.02 ve üzeri tarafından desteklenir ve küçük resimlerin üç farklı biçimde gömülmesine izin verir.

|Alan|Boyut (bayt)|Açıklama|
|---|---|---|
|APP0 işaretçisi|2|FF E0|
|Uzunluk|2|APP0 işaretçisi hariç segmentin uzunluğu|
|Tanımlayıcı|5|JFXX (4A 46 58 58 00) ASCII'de boş bayt tarafından sonlandırıldı|
|Küçük resim formatı|1|Aşağıdaki gömülü küçük resim için hangi veri formatının kullanıldığını belirtir:</br> 10 : JPEG formatı</br> 11 : Piksel başına 1 bayt paletlenmiş biçim</br> 13 : Piksel başına 3 bayt RGB biçimi|
|Küçük resim verileri|değişken||

## JFIF'in Diğer Görüntü Dosyası Formatlarına Dönüştürülmesi

JFIF, [PNG](/tr/image/png/), [JPG](/tr/image/jpg/) ve [PDF](/tr/pdf/) gibi popüler görüntü dosyası biçimlerine dönüştürülebilir.

## Referanslar ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

