---
date: 2020-08-12
keywords: flif, .flif, flif dosya formatı, flif dosyaları nasıl açılır, .flif uzantısı, flif uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF Dosya Biçimi
linktitle: FLIF
description: "FLIF dosya formatı ve FLIF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## FLIF dosyası nedir? ##

FLIF (Free Lossless Image Format), dosyaları için .flif uzantısını kullanan kayıpsız bir görüntü formatıdır. FLIF, sıkıştırma oranı açısından [PNG](/tr/image/png/), kayıpsız [WebP](/tr/image/webp/), kayıpsız BPG ve kayıpsız JPEG 2000'den daha iyi performans gösterdiğini iddia ediyor. FLIF, görüntünün herhangi bir kısmi indirilmesinin tüm görüntü için kayıplı bir kodlama olarak kullanılabilmesi nedeniyle aşamalı tarama kullanır.

## Kısa Tarih ##

FLIF, Eylül 2015'te duyuruldu ve alfa sürümü Ekim 2015'te yayınlandı. Eylül 2016'da FLIF'in ilk kararlı sürümü yayınlandı.

## FLIF Tasarım ##

FLIF, sıkıştırma için bir CABAC (Bağlama uyarlanabilir ikili aritmetik kodlama), MANIAC (Meta Uyarlamalı Sıfıra Yakın Tamsayı Aritmetik Kodlama) varyantını kullanır. MANIAC, Jon Sneyers ve Pieter Wuille tarafından geliştirilen bir entropi kodlama algoritmasıdır. MANIAC'ta bağlamlar, kodlama zamanında dinamik olarak öğrenilen karar ağaçlarının düğümleridir. Bu, bağlam modelini daha görüntüye özgü hale getirir ve daha iyi bir sıkıştırma sağlar. FLIF aşağıdaki özelliklere sahiptir:

- Kayıpsız sıkıştırmayı destekler
- Kodlayıcı ön işleme ile kayıplı sıkıştırmayı destekler
- Gri Tonlama, RGB ve RGBA'yı destekler
- Kanal başına 1 ila 16 bit renk derinliğini destekler
- Taramalı ve taramasız dosyaları destekler
- Kısmen indirilen dosyaların aşamalı kod çözmesini destekler
- Animasyonları destekler
- Katıştırılmış ICC renk profillerini, Exif ve XMP meta verilerini destekler
- Camera raw dosyalarını (RGGB) sıkıştırmak için sınırlı desteğe sahiptir

## FLIF Dosya Biçimi ##

Bir FLIF dosyası aşağıdaki dört bölümden oluşur:

## Ana Başlık ##

Ana başlık, genişlik, yükseklik, renk derinliği, çerçeve sayısı gibi ana meta verileri içerir.

|Tür|Değer|Açıklama|
|---|---|---|
|4 bayt|"FLIF"|Sihir|
|4 bit|3 = ni hareketsiz; 4 = hala; 5 = ni hayvan; 6 = i anim|Titreşim, animasyon|
|4 bit|1 = Gri Tonlama; 3 = RGB; 4 = RGBA|Kanal sayısı (nb_channels)|
|1 bayt|'0','1','2' ('0'=özel)|Kanal başına bayt (Bpc)|
|varent|genişlik-1|Genişlik|
|varent|boy-1|Boy|
|varint|nb_frames-2 (yalnızca animasyon ise)|Kare sayısı (nb_frames)|

## Meta veri parçaları ##

Bu bölüm, DEFLATE sıkıştırması kullanılarak kodlanmış Exif/XMP meta verileri, ICC renk profili vb. gibi piksel olmayanları içerir. Bu yığınlar, ayna boyutunun değişken sayıda bayt ile kodlanmış olması farkıyla, PNG parçalarına benzer şekilde tanımlanır. Parçaların adları 4 harf (4 bayt) veya isteğe bağlı olmayan bir yığını belirten 32'nin altında bir değer olabilir.

Aşağıda isteğe bağlı aynalara bir örnek verilmiştir:

|Yığın adı|Açıklama|İçerik (DEFLATE-açma işleminden sonra)|
|---|---|---|
|iCCP|ICC renk profili|ham ICC renk profili verileri|
|eXif|Exif meta verileri|"Exif\0\0" başlığını takip eden bir TIFF başlığı ve EXIF verileri|
|eXmp|XMP meta verileri|XMP, dolgusuz salt okunur bir xpacket içinde bulunur|

### Adlandırma kuralı ###

- **İlk Harf**: Kritik için büyük, kritik olmayan parçalar için küçük harf kullanılır.
- **İkinci Harf**: Genel için büyük, özel parçalar için küçük harf kullanılır
- **Üçüncü Harf**: Görüntünün doğru görüntülenmesi için gerekli aynalar için büyük harf kullanılır ve görüntünün görüntülenmesi için küçük harf önemli değildir.
- **Dördüncü Harf**: Büyük harf, körü körüne güvenle kopyalanabilen aynalar için kullanılır. Küçük harfli aynalar görüntü verilerine bağlıdır.

## İkinci Başlık ##

Bu, piksellerin gerçek kodlamasına ilişkin bilgileri içerir.

|Tür|Açıklama|Koşul|Varsayılan Değer|
|---|---|---|---|
|1 bayt|NUL baytı (0x00), bir FLIF16 bit akışının öbek adı||
|uni_int(1,16)|Kanalların piksel başına bit sayısı|Bpc == '0': tekrar(nb_channels)|8 if Bpc == '1', 16 if Bpc == '2'|
|uni_int(0,1)|İşaret: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Döngü sayısı|nb_frames > 1||
|uni_int(0,60_000)|ms olarak çerçeve gecikmesi|nb_frames > 1: tekrar(nb_frames)|
|uni_int(0,1)|İşaret: has_custom_cutoff_and_alpha|||
|uni_int(1.128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2.128)|alfa bölen|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|İşaret: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|değişken|Dönüşümler (aşağıya bakın)|||
|uni_int(1) = 0|Gösterge biti: dönüşümlerle tamamlandı|||
|uni_int(0,2)|Görünmez piksel tahmincisi|alpha_zero && taramalı && alfa aralığı sıfır içerir||

**Kanallar**

|Kanal numarası|Açıklama|
|---|----|
|0|Kırmızı veya Gri|
|1|Yeşil|
|2|Mavi|
|3|Alfa|

**Dönüşümler**

|Tür|Açıklama|
|---|---|
|uni_int(1) = 1|Gösterge biti: henüz yapılmadı|
|uni_int(0,13)|Dönüşüm tanımlayıcısı|
|değişken|Dönüşüm verileri (dönüşüme bağlıdır)|

Dönüştürme, daha iyi sıkıştırma için piksel verilerini değiştirmek ve gerçekte oluşan piksel değerlerini takip etmek için kullanılır.

## Piksel Verileri ##

Bu bölüm, MANIAC entropi kodlaması kullanılarak kodlanmış gerçek piksel verilerini içerir. Pikseller, taramalı veya taramasız kodlama kullanılarak kodlanabilir.

### Geçmeli yöntem ###

Bu yöntemde yakınlaştırma seviyeleri tanımlanır. Zoomlevel 0 tam görüntü için kullanılır, zoomlevel 1 tüm çift sayılı satırlar için kullanılır, zoomlevel 2 zoomlevel 1'in tüm çift sayılı sütunları için kullanılır. Başka bir deyişle, her çift sayılı zoomlevel 2k, görüntü, 1:2^k ölçeğinde. Yakınlaştırma seviyeleri en yüksekten en düşüğe doğru kodlanmıştır.

### Titreşimsiz yöntem ###

Bu yöntemde, MANIAC ağaçlarının kodlanması hemen ardından piksellerin kodlanmasıyla başlar.

## Referanslar ##

- [FLIF - Vikipedi](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

