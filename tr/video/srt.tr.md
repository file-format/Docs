---
date: 2019-10-11
keywords: srt, .srt, srt dosya biçimi, .srt dosya biçimi, .srt uzantısı, srt uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "SRT dosya formatı ve SRT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: SRT Dosya Biçimi
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## SRT dosyası nedir? ##

SRT (SubRip dosya formatı), .srt uzantısıyla SubRip dosya formatında kaydedilen basit bir altyazı dosyasıdır. Sıralı sayıda altyazı, başlangıç ve bitiş zaman damgaları ve altyazı metni içerir. SRT dosyaları, oluşturulduktan sonra video içeriğine alt yazı eklenmesini mümkün kılar.

## SRT dosya Yapısı ##

SRT dosyasında her altyazının dört bölümü vardır.

1. Altyazının numarasını veya konumunu gösteren bir sayısal sayaç.
1. --> karakterlerle ayrılmış altyazının başlangıç ve bitiş zamanı
1. Bir veya daha fazla satırda altyazı metni.
1. Alt başlığın sonunu gösteren boş bir satır.

### SRT Örneği ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Saati belirtmek için *saat:dakika:saniye,milisaniye (00:00:00,000)* formatı kullanılır.

## SRT dosyalarının biçimlendirilmesi ##

SRT dosyalarının biçimlendirmesi HTML etiketlerinden türetilmiştir. SRT dosyası için biçimlendirme etiketleri aşağıda listelenmiştir.

| Efekt | Etiketler |
| --- | --- |
|Kalın|**\ <b>...\</b> ** veya {b}...{/b}|
|İtalik|**\ <i>...\</i> ** veya **{i}...{/i}**|
|Alt çizgi|**\ <u>...\</u> ** veya **{u}...{/u}**|
|Yazı Tipi Rengi|**\ <font color="white">...\</font> **|
|Satır Konumu|**{\a3}** (metnin 3. satırda görünmeye başlaması gerektiğini gösterir)

## SubRip Yazılımı ##

SubRip, Windows üzerinde çalışan ücretsiz bir yazılım programıdır. Farklı video formatlarından altyazıları ve zamanlamalarını çıkarır ve altyazıları SRT formatında kaydeder. SubRip, canlı videodan, diğer video dosyalarından ve DVD'lerden altyazıları çıkarmak için optik karakter tanımayı kullanır.

## Referanslar ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
