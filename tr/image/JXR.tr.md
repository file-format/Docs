---
date: 2020-08-12
keywords: jxr, .jxr, jxr dosya formatı, jxr dosyaları nasıl açılır, .jxr uzantısı, jxr uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR Dosya Biçimi
linktitle: JXR
description: "JXR dosya formatı ve JXR dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## JXR dosyası nedir? ##

JPEG XR (JPEG genişletilmiş aralık), sürekli tonlu fotoğrafik görüntüler için bir dosya formatıdır. Microsoft tarafından geliştirilen HD Photo'ya dayalı bir hareketsiz görüntü sıkıştırma standardıdır. Hem kayıplı hem de kayıpsız sıkıştırmayı destekler.

## Kısa Tarih ##

Windows Media Photo ilk olarak Microsoft tarafından WinHEC 2006'da duyuruldu. Kasım 2006'da HD Photo olarak yeniden adlandırıldı. JPEG XR, 19 Haziran 2009'da Uluslararası Standart ISO/IEC 29199-2 olarak onaylandı. ITU-T ve ISO/IEC bir önerge yayınladı format belirtimi (ITU-T T.833 | ISO/IEC 29199-3), uygunluk testi seti (ITU-T T.834 | ISO/IEC 29199-4) ve referans yazılımı (ITU-T T.835 | ISO /IEC 29199-5) 2010'da görüntü kodlama spesifikasyonunun tamamlanmasından sonra JPEG XR için. JPEG XR için iş akışı mimarisini açıklayan bir teknik rapor 2011'de yayınlandı.

## JPEG XR Tasarım ##

JPEG ile karşılaştırıldığında, JPEG XR aşağıdakiler dahil çeşitli iyileştirmeler sunar:

- **Daha İyi Sıkıştırma**: JPEG XR, daha yüksek sıkıştırma oranları sunar.
- **Kayıpsız Sıkıştırma**: JPEG XR, kayıpsız sıkıştırmayı destekler.
- **Döşeme Yapısı**: JPEG XR görüntüsü, her bölgenin kodunun ayrı ayrı çözülebileceği döşeme bölgelerine bölünebilir.
- **Daha fazla renk doğruluğu**: JPEG XR, RGB renk alanını kullanan görüntüleri desteklemek için YCoCg renk alanına dahili dönüştürme içerir. JPEG XR ayrıca bileşen başına 16 bit (piksel başına 64 bit) tamsayı CMYK renk modelini destekler. JPEG XR, HDR görüntüler için RGBE paylaşımlı üslü kayan noktalı renk formatını destekler. JPEG XR, gri tonlamalı ve çok kanallı renk kodlamalarını da destekler.
- **Şeffaflık Haritası**: JPEG XR, saydamlık için alfa kanalını destekler.
- **Sıkıştırılmış alan görüntüsü değişikliği**: JPEG XR görüntüleri kayıplı kodlamaya dönüştürülebilir, çözünürlüğü azaltılabilir, kırpılabilir, ters çevrilebilir, döndürülebilir ve dosyanın kodu tamamen çözülmeden döşeme yapısı değiştirilebilir.
- **Meta Veri Desteği**: JPEG XR resim dosyası, birden fazla cihazda tutarlı renk temsili için ICC renk profili içerebilir. Biçim ayrıca Exif ve XMP meta veri biçimlerini de destekler.

## Konteyner Biçimi ##

JPEG XR görüntü verileri, bir Görüntü Dosyası Dizini (IFT) etiketleri tablosu kullanılarak TIFF benzeri kapsayıcı biçiminde saklanabilir. Bir JXR dosyası, IFD etiketlerinde aşağıdakileri içerir:

- Görüntü verileri: Bitişik, kendi kendine yeten görüntü verileridir.
- İsteğe bağlı alfa kanalı verileri: Bu varsa, görüntü verileri ayrı ayrı sıkıştırılarak saydamlığı desteklemeyen uygulamaların desteklenmesi sağlanabilir.
- Meta veriler
- İsteğe bağlı XMP meta verileri
- İsteğe bağlı Exif meta verileri

TIFF biçimini temel aldığından, 4 GB dosya boyutu sınırı gibi tüm TIFF biçimi sınırlamalarını devralır.

## Referanslar ##

- [JPEG XR - Vikipedi](https://en.wikipedia.org/wiki/JPEG_XR)

