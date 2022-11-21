---
date: 2021-03-21
keywords: alac, alac dosya formatı, .alac uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "ALAC dosya formatı ve ALAC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: ALAC - Apple Kayıpsız Ses Codec Dosya Biçimi
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## ALAC dosyası nedir?

ALAC dosya formatı, MPEG-4 uyumlu QuickTime kapsayıcısını kullanan Apple Lossless Audio Codec'tir (ALAC). 2004 yılında tescilli dosya formatı olarak tanıtıldı, 2011 yılına kadar Apple onu açık kaynak ve telifsiz olarak kullanıma sundu. Biçim, [FLAC](/tr/audio/flac/) (Ücretsiz Kayıpsız Ses Codec Bileşeni) biçimine benzer, ancak buna kıyasla daha fazla sıkıştırma sunar. [AAC](/tr/audio/aac/) veya [MP3](/tr/audio/mp3/)'ye göre daha iyi ses alternatifi sunar. ALAC codec'i ile kodlanmış ses dosyaları Apple QuickTime, Apple iTunes ve K-Lite codec'li Microsoft Windows Media Player kullanılarak açılabilir.

## ALAC Dosya Biçimi

ALAC codec bileşenini temel alan dosyalar, geliştiricinin referansı için [GitHub'da açık kaynak](https://github.com/macosforge/alac) olarak sunulan ikili dosyalardır. ALAC kodlayıcı ve kod çözücü için kaynakları içerir. Apple ayrıca Core Audio Format (CAF) ve [WAVE](/tr/audio/wav/) dosyalarına/dosyalarından ses verilerini okumak ve yazmak için "alacconvert" adlı bir komut satırı yardımcı programı da sağlamıştır. ALAC dosya formatı hakkında bazı önemli noktalar aşağıdadır.

1. "Bit Derinlikleri" - 16, 20, 24 ve 32 bit.
1. "Örnekleme Hızı" - 1 ila 384.000 Hz arasında herhangi bir isteğe bağlı tamsayı örnekleme hızı. 4.294.967.295 (2^32 - 1) Hz'e kadar teorik oranlar desteklenebilir.
1. "Paket Boyutu" - Varsayılan paket boyutu varsayılan olarak paket başına 4096 örnek ses karesidir. Diğer paket boyutları kesinlikle mümkündür. Ancak, varsayılan olmayan paket boyutlarının Apple Lossless'ı destekleyen tüm donanım aygıtlarında düzgün çalışması garanti edilmez. 16.384 örnek çerçevenin üzerindeki paketler desteklenmez.
1. `Desteklenen Kanallar` - Birden sekize kadar kanalı destekler. Her kanal aşağıdaki bilgi sırasına sahiptir.

|Num Chan| Sipariş|
|---|---|
|1 |tek|
|2 |stereo (Sol, Sağ)|
|3 |MPEG 3.0 B (Merkez, Sol, Sağ)|
|4 |MPEG 4.0 B (Merkez, Sol, Sağ, Orta Çevre)|
|5 |MPEG 5.0 D (Merkez, Sol, Sağ, Sol Çevre, Sağ Çevre)|
|6 |MPEG 5.1 D (Merkez, Sol, Sağ, Sol Çevre, Sağ Çevre, Düşük Frekans Efektleri)|
|7 |Apple AAC 6.1 (Merkez, Sol, Sağ, Sol Çevre, Sağ Çevre, Orta Çevre, Düşük Frekans Efektleri)|
|8 |MPEG 7.1 B (Merkez, Sol Merkez, Sağ Merkez, Sol, Sağ, Sol Çevre, Sağ Çevre, Düşük Frekans Efektleri)|

## Referanslar

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Apple Kayıpsız Ses Codec'i](https://macosforge.github.io/alac/)
* [macosforge - GitHub'da alac](https://github.com/macosforge/alac)

