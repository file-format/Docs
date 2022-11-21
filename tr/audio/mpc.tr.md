---
date: 2021-03-21
keywords: mpc, Musepack dosya formatı, .mpc uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "MPC dosya formatı ve MPC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: MPC - Musepack Ses Sıkıştırma Dosyası Biçimi
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## MPC dosyası nedir?

.mpc uzantılı bir dosya, yüksek kaliteye güçlü bir vurgu yaparak ses sıkıştırma kullanan bir [Musepack](https://musepack.net/) ses dosyası biçimidir. Bu, orijinal [WAV](/tr/audio/wav/) dosyası ile sıkıştırılmış MPC dosyası arasındaki ses kalitesi farklılıklarını fark etmemenizi bile mümkün kılar. Yüksek düzeyde optimize edilmiş sıkıştırma elde etmek için MPEG-1 Layer-2 algoritmalarını kullanır. Musepack MPC dosya formatı, BSD/GNU LGPL lisansı ile açık kaynaklıdır. Musepack'in [SVN deposu](http://svn.musepack.net/) codec için en son güncellenen kodun alınmasına olanak tanır. MPC dosyalarını açabilen uygulamalar, diğerlerinin yanı sıra VLC Media Player, JetAudio ve Winamp'ı içerir.

## MPC Dosya Biçimi

MPC dosyası, ses dosyalarını sıkıştırmak için MPEG-1 Layer-2 algoritmalarını kullanır. Kapsayıcıdan bağımsız bir formattır ve ayrıca ham akış kodlamasına izin verir. Biçim, herhangi bir dahili kırpma kullanmaz ve örnek-hassas kesme ile akış halindedir. Paketlenmiş akışı, [MKV](/tr/video/mkv/) gibi ses ve video kapsayıcılarına çoğullamaya izin verir.

## Referanslar

* [Musepack MPC - Wikipedia](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)

