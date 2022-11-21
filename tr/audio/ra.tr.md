---
date: 2019-12-13
keywords: ra, ra dosya biçimi, .ra uzantısı, gerçek ses dosyası biçimi, ra ses biçimi, RealAudio dosya biçimi
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RA dosya formatı ve RA dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: RA Dosya Biçimi
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## .ra dosyası nedir?

RealAudio (RA), Real Networks, Inc. tarafından geliştirilen ve Nisan 1995'te piyasaya sürülen tescilli bir ses formatıdır. Dosyaları için .ra uzantısını kullanır. Düşük bit hızı ve yüksek kaliteli ses codec bileşenleri kullanır. RA, birçok internet radyo istasyonu tarafından internet üzerinden ses akışı için kullanıldı. BBC web sitesi, RA'yı 2009 yılına kadar yoğun bir şekilde kullandı, ancak Mart 2011'de kullanımdan kaldırıldı.

## RealNetworks tarafından Dosya Uzantısı ##

RealNetworks, ses için RA dosya formatını kullandı. RealNetworks, 1997'de .rv uzantısıyla video formatı ([RealVideo](/tr/video/rv/)) sunmaya başladı. Ses ve video formatlarının kombinasyonu için [RealMedia (RM)](/tr/video/rm/) kullanıldı. RealProduce'un (Real'in kodlayıcısı) en son sürümüyle, video dosyaları için RV biçimi ve VBR (Değişken bit hızı) video dosyaları için [RealMedia Değişken Bit Hızı (RMVB)](/tr/video/rmvb/) biçimi kullanılır.

## Ses Akışı ##

RA, akış ortamı formatı olarak geliştirilmiştir ve HTTP kullanılarak akış gerçekleştirilebilir. Ses dosyası, dosyanın ilk kısmı alınır alınmaz çalmaya başlar ve dosyanın geri kalanı indirildikçe çalmaya devam eder.

RealAudio'nun ilk sürümü, ses akışı için tescilli PNA veya PNM protokolünü kullandı. Daha sonra bağlantıları yönetmek için IETF standartlaştırılmış RTSP'ye (Gerçek Zamanlı Akış Protokolü) geçtiler. Veri göndermek için RDT (Gerçek Veri Aktarımı) protokolünü kullandılar. Protokol başlangıçta gizli tutuldu, ancak daha sonra Helix projesi aracılığıyla bir kısmı kamuoyuna açıklandı.

RealAudio dosyalarının akışı için, sayfaların çoğu RAM (Real Audio Metadata) veya SMIL (Senkronize Multimedya Entegrasyon Dili) dosyasına bağlanır. Bu dosya, kullanıcının medya oynatıcısını yüklemek ve dosyada bulunan URL'den ses akışı yapmak için kullanılır.

## RealAudio Ses Codec'leri ##

Burada, her biri dört karakterli bir kodla tanımlanan ses codec bileşenlerinin ve onu tanıtan RealAudio sürümünün bir listesi bulunmaktadır.

|Codec|RealAudio Sürümü|
|---|---|
|lpcJ ve 14_4|1|
|28_8|2|
|dnet|3|
|sip|4/5|
|aşçı|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## Referanslar ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

