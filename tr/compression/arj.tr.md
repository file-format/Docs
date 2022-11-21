---
date: 2019-12-09
keywords: arj, .arj, arj dosya formatı, arj dosyaları nasıl açılır, .arj uzantısı, arj uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ Dosya Biçimi
linktitle: ARJ
description: "ARJ dosya formatı ve ARJ dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## ARJ dosyası nedir? ##

ARJ (Archived by Robert Jung), Robert K. Jung tarafından geliştirilen yüksek verimli bir sıkıştırılmış arşiv dosyasıdır. ARJ, 1990'ların başında DOS ve Windows'un ilk sürümleri için geliştirildi. ARJ dosyaları, tüm bu dosyaları takip etmeniz gerekmediğinden ve işlenecek yalnızca tek bir dosya olduğundan, çok sayıda dosyayı yedeklemek veya paylaşmak için kullanışlıdır. ARJ arşiv dosyaları için .arj uzantısı kullanılır.

## ARJ Dosya Biçimi ##

Bir ARJ dosyası iki tür başlık içerir:

- Ana başlık: Arşivin başında bir ana başlık vardır.
- Yerel başlıklar: Yerel başlıklar her dosyadan önce bulunur.

|Ofset|Tür|Sayı|Açıklama|
|---|---|---|---|
|0000h|kelime|1|ID=0EA60h|
|0002h|word|1|temel başlık boyutu|
|0004h|bayt|1|Başlığın boyutu|
|0005h|byte|1|Arşivleyici sürüm numarası|
|0006h|bayt|1|Minimum sürüm numarası gerekli|
|0007h|bayt|1|Ana İşletim Sistemi:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMİGA</br> 4 - MAC-OS (Sistem xx)</br> 5 - OS/2</br> 6 - ELMA GS</br> 7 - ATARI SOKAK</br> 8 - NeXT</br> 9 - VAX VMS|
|0008h|byte|1|Dahili İşaretler, bit eşlemli:</br> 0 - şifre / şifre yok</br> 1 - ayrılmış</br> 2 - dosya bir sonraki diskte devam eder</br> 3 - dosya başlangıç konumu alanı mevcut</br> 4 - yol çevirisi ( "\" - "/" )|
|0009h|bayt|1|Sıkıştırma yöntemi:</br> 0 - saklandı</br> 1 - en çok sıkıştırılmış</br> 2 - sıkıştırılmış</br> 3 - daha hızlı sıkıştırılmış</br> 4 - en hızlı sıkıştırılmış|
|000Ah|bayt|1|Dosya türü:</br> 0 - ikili</br> 1 - 7 bitlik metin</br> 2 - yorum başlığı</br> 3 - dizin</br> 4 - cilt etiketi|
|000Bh|bayt|1|ayrılmış|
|000Ch|dword|1|MS-DOS formatındaki orijinal dosyanın Tarih/Saati|
|0010h|dword|1|Sıkıştırılmış dosyanın boyutu|
|0014h|dword|1|Orijinal dosyanın boyutu"|
|0018h|dword|1|orijinal dosyanın CRC-32'si|
|001Ah|word|1|Dosya adındaki dosyabelirtimi konumu|
|001Ch|word|1|Dosya öznitelikleri|
|001Eh|word|1|Ana veri|
|?|dword|1|Genişletilmiş dosya başlangıç konumu|
|????h|dword|1|CRC-32 temel başlığın|
|????h|word|1|İlk genişletilmiş başlığın boyutu|
|????h+"SIZ"+2|dword|1|CRC-32, genişletilmiş başlığın|
|????h+"SIZ"+6|byte|?|Sıkıştırılmış dosya|

## Referanslar ##

- [ARJ - Vikipedi](https://en.wikipedia.org/wiki/ARJ)

