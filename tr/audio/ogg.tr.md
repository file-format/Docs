---
date: 2019-12-13
keywords: ogg, ogg dosya formatı, .ogg uzantısı, ogg ses formatı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "OGG dosya formatı ve OGG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: OGG Dosyası - Ogg Vorbis Ses Dosyası
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## OGG dosyası nedir?

OGG, .ogg uzantısıyla kaydedilen bir Ogg Vorbis Sıkıştırılmış Ses Dosyasıdır. OGG dosyaları, ses verilerini depolamak için kullanılır ve sanatçı ve parça bilgilerini ve meta verileri de içerebilir. OGG, Xiph.Org Foundation tarafından sağlanan ücretsiz ve açık bir kapsayıcı biçimidir.

## OGG Dosya Formatının Kısa Tarihi

Ogg projesi 1993 yılında daha büyük bir projenin parçası olarak başladı ve Squish olarak adlandırıldı, ancak mevcut bir ticari marka nedeniyle OggSquish olarak yeniden adlandırıldı. Modern ses uygulamaları için esnek bir sıkıştırılmış ses formatı yaratma girişimi olarak tanımlandı. OGG referansı, 2 Eylül 2000'de Vorbis'ten ayrıldı.

OGM, OGG'de resmi video desteği olmaması nedeniyle 2002 yılında kuruldu. Bu, videonun Microsoft DirectShow çerçevesinden OGG tabanlı bir paketleyiciye yerleştirilmesine izin verdi. 2006 yılına gelindiğinde, OGG birçok video oyun motoru tarafından destekleniyordu ve yaygın olarak ücretsiz içeriği kodlamak için kullanılıyordu. Özgür Yazılım Vakfı, MP3'e üstün bir alternatif olarak Vorbis'in kullanımını artırmak için 15 Mayıs 2007'de bir kampanya başlattı. 30 Haziran 2009 itibarıyla OGG, Firefox 3.5'in HTML5 uygulaması tarafından desteklenen tek kapsayıcı biçimiydi.

## OGG Dosya Biçimi

OGG formatı veri parçalarından oluşur. Her parçaya Ogg sayfası denir. Her sayfa, Ogg Formatını tanımlamak için "OggS" ile başlar. Başlık, her sayfayı bir dizinin parçası olarak tanımlayan seri numarasını ve sayfa numarasını içerir. Sayfa aşağıdaki bileşenlerden oluşmaktadır.

- **Sayfa Başlığı**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Değer | Açıklama |
| --- | --- | --- |
| 0 | 0x01 | Sayfanın ilk paketinin, önceki paketin mantıksal bit akışındaki devamı olduğunu belirtir. |
| 1 | 0x02 | Bu sayfanın mantıksal bit akışındaki ilk sayfa olduğunu gösterir. |
| 2 | 0x04 | Bu sayfanın mantıksal bit akışındaki son sayfa olduğunu gösterir. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Meta veriler**: VorbisComment, meta verileri depolamak için en yaygın olarak desteklenen mekanizmadır. Diğer mekanizmalar aşağıdakileri içerir:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referanslar ##

- [OGG - Vikipedi](https://en.wikipedia.org/wiki/Ogg)

