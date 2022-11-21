---
date: 2019-12-09
keywords: arc, .arc, arc dosya formatı, arc dosyaları nasıl açılır, .arc uzantısı, arc uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC Dosya Biçimi
linktitle: ARC
description: "ARC dosya formatı ve ARC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## .arc dosyası nedir?

ARC, System Enhancement Associates (SEA) tarafından geliştirilen kayıpsız bir veri sıkıştırma ve arşivleme biçimidir. Hem dosya biçimi hem de onu oluşturan uygulama ARC olarak adlandırılır. ARC, sıkıştırma ve birden çok dosyayı aynı dosyada arşivleme özelliklerini birleştirdiği için çevirmeli BBS'nin ilk günlerinde çok popülerdi. ARC daha sonra daha iyi sıkıştırma oranları sunan [ZIP](/tr/compression/zip/) ile değiştirildi.

.arc dosya uzantısı, İnternet Arşivi tarafından birden fazla web kaynağını depolamak için kullanılan ARC formatı, FreeArc arşivleyici tarafından kullanılan farklı bir ARC formatı, Nintendo tarafından kaynaklar için kullanılan farklı bir format vb. .

## ARC Dosya Formatının Kısa Tarihi

ARC programı, System Enhancement Associates'ten Thom Henderson tarafından 1985 yılında yazılmıştır. Bu program, dosyaları tek bir arşiv dosyasında gruplandırmış ve ayrıca sıkıştırmıştır. ARC programı tarafından oluşturulan dosyalar .arc uzantısını kullandı. SEA, 1986'da ARC'nin kaynak kodunu yayınladı ve ARC, 1987'de Howard Chu tarafından Unix ve Atari ST'ye taşındı.

Phil Katz, dosyaları arşivlemek ve çıkarmak için PKARC ve PKXARC'yi geliştirdi. Dosyalar ARC dosya biçimiyle çalıştı ve önemli ölçüde daha hızlıydı. ARC'den farklı olarak Katz, sıkıştırma ve arşivleme işlevlerini iki farklı dosya arasında böldü ve bu da onları çalıştırmak için bellek gereksinimini azalttı.

SEA ve Katz arasındaki davanın ardından SEA, shareware pazarından çekildi ve tam ekran kullanıcı arabirimli ARC+Plus'ı geliştirdi. ARC formatı artık PC'de yaygın değil.

## ARC Dosya Biçimi

ARC dosyası, aşağıda gösterildiği gibi bir dosya başlığı ve dosya dizisinden ve ardından arşiv sonu işaretçisinden oluşur.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC Dosya Başlığı ###

|Ofset|Etiket|Tür|Değer|Açıklama|
|---|---|---|---|---|
|00|ARCID |DB|1 Milyar Dolar| |
|01|ARCMTD|DB|00|Yöntem|
|02|ARCFNT|DS|12|dosya adı|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Sıkıştırılmış boyut|
|13|ARCDAT|DW|0000|Dosya tarihi (MSDOS)|
|15|ARCTIM|DW|0000|Dosya zamanı (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Sıkıştırılmamış boyut|
|1D|ARCFIL|DS|ARCNSZ| |

### Sıkıştırma Yöntemleri ###

Sıkıştırma yöntemi baytı, kullanılan sıkıştırma yöntemini gösterir. ARC dosyası için kullanılan sıkıştırma yöntemleri aşağıdadır.

|Yöntem|Ad|Açıklama|
|---|---|---|
|0|Kayıtlı|Sıkıştırma kullanılmaz|
|1|Paketlenmiş|Tekrarlanan uzunluk kodlaması (RLE)|
|2|Sıkıştırılmış|Huffman kodlaması|
|3|Crunched|4K ara belleğe sahip LZW, 12 bit kodlar|
|4|Crunched|Önce paketleme, ardından 12 bitlik LZW 4K tampon|
|5|Crunched|Paketleme, LZW, 4K arabellek, değişken uzunluk (9-12 bit)|
|6|Ezilmiş|LZW, 8K arabellek, değişken uzunluk (9-13 bit)|
|7|Crushed|Paketleme, ardından LZW 8K arabellek, 2-13 bit (PAK 1.0)|
|8|Distill|8K ara belleğe sahip Dinamik Huffman (PAK 2.0)|

## Referanslar

- [ARC (dosya formatı) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

