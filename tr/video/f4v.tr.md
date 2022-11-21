---
date: 2019-10-11
keywords: f4v, .f4v, f4v dosya formatı, .f4v dosya formatı, .f4v uzantılı, f4v uzantılı, f4v video formatı, f4v dosyası nasıl açılır, f4v dosyası nedir
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "F4V dosya formatı ve F4V dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin"
title: F4V Dosya Biçimi
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## F4V dosyası nedir? ##

F4V (Flash MP4 Video Dosyası), .f4v uzantısıyla kaydedilen bir video dosyasıdır. ISO tabanlı medya dosyası formatına (MPEG-4 Part 12) dayanmaktadır. [MP4](/tr/video/mp4/)'e çok benzer, bu nedenle gayri resmi olarak Flash MP4 olarak da adlandırılır. [FLV](/tr/video/flv/), H.264/ACC içeriklerini aktarırken sınırlamalara sahipti, bu da Adobe Systems'in yeni F4V formatını oluşturmasına neden oldu. Flash Player, Flash Player 9 Güncelleme 3'ün yayınlanmasından bu yana F4V dosyalarını oynatabilir.

## F4V dosyalarının yapısı ##

F4V dosya formatı, ISO tabanlı medya dosyası formatına (MPEG-4 Kısım 12) dayalıdır ve MP4 formatına çok benzer. Yapıyla ilgili ayrıntılar için lütfen [MP4](/tr/video/mp4/) sayfasına bakın. F4V ve MP4 arasındaki en büyük fark, F4V'nin saklayabileceği meta veri biçimleridir. Aşağıda verilenler, F4V formatı tarafından desteklenen meta veri formatlarının listesidir.

- **Etiket kutusu**: Film (moov) kutusu içinde ek dört isteğe bağlı etiket kutusu (auth, title, dscp, cprt).
- **XMP Meta Veri kutusu**: Bu kutu, Film (moov) kutusundan hemen sonra gelir. Bununla dosya, XMP meta verilerini ActionScript aracılığıyla bir SWF filmine iletebilir.
- **ilst kutusu**: Bu kutu, Meta (meta) kutusunun içinde bulunur ve bir dizi meta veri etiketi içerebilir. Desteklenen veri türleri aşağıda verilmiştir.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata box**: Medya Veri Kutusu (mdat) içindeki metin örnekleri (metin veya tx3g). Aşağıdaki meta veri kutularını içerebilir.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referanslar ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

