---
date: 2020-08-12
keywords: bpg, .bpg, bpg dosya formatı, bpg dosyaları nasıl açılır, .bpg uzantılı, bpg uzantılı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG Dosya Biçimi
linktitle: BPG
description: "BPG dosya formatı ve BPG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## BPG dosyası nedir? ##

BPG (Better Portable Graphics), Fabrice Bellard tarafından 2014 yılında dijital görüntüler için oluşturulmuş bir dosya formatıdır. BPG daha fazla sıkıştırma veya boyut açısından verimli olduğundan, JPEG'in yerine BPG'yi önerdi. BPG, HEVC (Yüksek Verimli Video Kodlama) video sıkıştırma standardının çerçeve içi kodlamasını kullanır.

BPG, taşınabilir ve IoT cihazlarında çalışmak için belleği verimli kullanan taşınabilir bir biçim olarak tasarlanmıştır. Şu anda web tarayıcıları BPG biçimini desteklememektedir, ancak web siteleri yine de Bellard tarafından yazılmış bir JavaScript kitaplığı kullanarak BPG görüntüleri sunabilir. BPG, örnek başına 14 bit'e kadar HEVC'nin Ana 4:4:4 16 Fotoğraf profilini kullanır.

## Özellikler ##

BPG konteyner formatı, HEVC'de kullanılan ham bit akışı yerine genel bir görüntü formatıdır. BPG, 4:4:4, 4:2:2 ve 4:2:0 renk biçimlerini destekler. Alfa kanalı ayrıca ayrı kodlanmış bir ekstra kanal veya CMYK görüntüsünün dördüncü kanalı ile desteklenir. BPG, Exif, ICC profilleri ve XMP için meta veri desteği sağlar. BPG, YCbCr (ITU-R BT.601, BT.709 ve BT.2020 (sabit olmayan parlaklık))), YCgCo, RGB, CMYK ve gri tonlamalı renk uzayını destekler. BGP ayrıca animasyonu ve kayıplı ve kayıpsız HEVC veri sıkıştırmasını da destekler.

## Referanslar ##

- [Daha İyi Taşınabilir Grafikler - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

