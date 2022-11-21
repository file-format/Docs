---
date: 2019-10-11
keywords: flv, .flv, flv dosya biçimi, .flv dosya biçimi, .flv uzantısı, flv uzantısı, flv video biçimi
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLV dosya formatı ve FLV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: FLV Dosya Biçimi
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## FLV dosyası nedir? ##

FLV (Flash Video), .flv uzantılı bir kapsayıcı dosya biçimidir. FLV, Adobe Flash Player veya Adobe Air kullanılarak internet üzerinden ses/video içeriği iletmek için kullanılır. FLV dosyalarındaki veriler, SWF dosyalarıyla aynı şekilde kodlanır. 2003 yılında Flash Player 7'ye doğrudan destek eklendi. Adobe sistemleri, FLV'nin kısıtlamaları nedeniyle 2007'de F4V'yi oluşturdu.

### Kodlama ###

FLV dosyaları, H.263 video standardının tescilli bir çeşidi olan Sorenson Spark'ın video bit akışlarını içerir. Flash Player 6 ve 7 için gerekli sıkıştırma biçimidir. On2 TrueMotion VP6 video bit akışları için Flash Player'ın 8. sürümü desteği. Flash Player 8 ve üstü için önerilen sıkıştırma formatıdır. FLV, MP3, Nellymoser Asao Codec ve açık kaynaklı Speex codec'te sesi destekler. Ayrıca sıkıştırılmamış sesi veya ADPCM formatındaki sesi de destekler. AAC (HE-AAC/AAC SBR, AAC Ana Profili ve AAC-LC), Flash Player 9'un son sürümleri tarafından desteklenir.

## Yapı ##

FLV dosyaları Başlık ve Paketlerden oluşur. Bir FLV dosyası Başlık ile başlar. Başlık aşağıdaki alanlara sahiptir.

- **İmza**: Değeri FLV'dir.
- **Sürüm**: Varsayılan değeri 1'dir. Yalnızca 0x01 geçerlidir.
- **İşaretler**: Ses için 0x04 ve video için 0x01 kullanılır, bu nedenle hem ses hem de video için 0x05 kullanılır.
- **Başlık Boyutu**: Varsayılan değer 9'dur. Daha yeni genişletilmiş bir başlığı atlamak için kullanılır.

Başlıktan sonra Paketler gelir. FLV dosyası, 15 baytlık başlıkları olan FLV etiketleri adı verilen birden çok pakete bölünmüştür. Paketler, ses, video, komut dosyaları, şifreleme bilgileri ve yük için meta verileri içerir. FLV paketleri aşağıdaki alanlara sahiptir.

- **Ayrılmış**: FMS için ayrılmıştır ve 0 olmalıdır.
- **Filtre**: Paketlerin filtrelenip filtrelenmediğini gösterir.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Paket Türü**: Bu, paketteki içeriğin türünü tanımlar.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Veri Boyutu**: Bu, mesajın uzunluğunu belirtir.
- **Zaman Damgası Alt**: Bu, zaman damgasını etiket verilerinin geçerli olduğu milisaniye cinsinden saklar. İlk paket için NULL olarak ayarlanmıştır.
- **Zaman Damgası Üstü**: Bir uint32_be değeri oluşturmak için uzantı.
- **Akış Kimliği**: Bu, ilk akış için NULL olarak ayarlanır.
- **Yük Verisi**: Bu, paket tipine dayalı verilerdir.

## Referanslar ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

