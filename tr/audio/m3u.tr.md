---
date: 2019-12-13
keywords: m3u, m3u dosya formatı, .m3u uzantısı, m3u multimedya çalma listesi, m3u çalma listesi formatı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "M3U dosya formatı ve M3U dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: M3U Dosya Biçimi
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## M3U dosyası nedir? ##

M3U (MP3 URL), .m3u uzantısıyla saklanan bir ses çalma listesi dosyasıdır. M3U gerçek bir ses dosyası değildir, sadece ses ve bazen de video dosyalarına işaret eder. M3U, Fraunhofer tarafından Winplay3 yazılımı ile kullanılmak üzere geliştirilmiştir. Ayrıca çeşitli medya oynatıcılar ve yazılımlar tarafından da desteklenmektedir.

## M3U Dosya Biçimi

M3U dosya biçimi için resmi bir belirtim yoktur, fiili bir standarttır. M3U, metin yerel sistemin varsayılan Unicode olmayan kodlamasında kodlanmışsa .m3u uzantısını veya metin UTF-8 olarak kodlanmışsa .m3u8 uzantısını kullanan bir düz metin dosyasıdır. M3U dosyasındaki her giriş aşağıdakilerden biri olabilir:

- Dosyanın mutlak yolu
- M3U dosyasına göre dosya yolu.
- URL

### Genişletilmiş M3U ###

Genişletilmiş M3U'da, parametreleri varsa "#" ile başlayan ve iki nokta üst üste(:) ile biten ek yönergeler tanıtılır. Aşağıda, genişletilmiş M3U için yönergelerin bir listesi verilmiştir.

- **#EXTM3U** - Genişletilmiş M3U'yu belirten dosya başlığıdır ve dosyanın ilk satırı olmalıdır.
- **#EXTENC:** - Metin kodlama. Dosyanın 2. satırı olmalıdır.
- **#EXTINF:** - Parça bilgileri ve diğer ek özellikler için kullanılır.
- **#PLAYLIST:** - Oynatma listesinin başlığı
- **#EXTGRP:** - Ad gruplandırmaya başla
- **#EXTALB:** - Albüm bilgisi
- **#EXTART:** - Albüm sanatçısı
- **#EXTGENRE** - Albüm Türü
- **#EXTM3A** - Albüm parçaları veya bölümleri için tek dosya çalma listesi.
- **#EXTBYT:** - Bayt cinsinden dosya boyutu.
- **#EXTBIN:** - Bunu ikili veriler takip eder.
- **#EXTIMG:** - Logo, Kapak veya diğer resimler.

### HLS M3U ###

HLS (HTTP Canlı Akış), iOS aygıtlarına ses ve radyo akışı sağlamak için Apple tarafından oluşturuldu. UTF-8 kodlu genişletilmiş M3U'ya dayanmaktadır. 2017 yılında IETF tarafından RFC 8216 olarak standardize edilmiştir. HLS oynatma listesinin etiketleri "#EXT-X-" ile başlar. Aşağıda HLS için etiketlerin bir listesi verilmiştir.

- **EXT-X-VERSION** - Medya ve sunucusuna göre dosyanın uyumluluk sürümünü gösterir.
- **#EXT-X-START:** - Çalma listesi için tercih edilen başlangıç noktasını belirtir.
- **#EXT-X-PLAYLIST-TYPE:** - Çalma listesi türünü (EVENT veya VOD) sağlar.
- **#EXT-X-TARGETDURATION:** - Maksimum Segment süresini belirtir.
- **#EXT-X-MEDIA-SEQUENCE:** - Ortam Sıra Numarasını gösterir.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Tüm ortam örneklerinin bağımsız olduğunu ve diğer bölümler olmadan kodun çözülebileceğini gösterir.
- **#EXT-X-MEDIA:** - Aynı içeriğin alternatif Yorumlarını içeren Medya Oynatma Listelerini ilişkilendirmek için kullanılır.
- **#EXT-X-STREAM-INF:** - Yorumlamaların parçası olan bir Varyant Akışı belirtir.
- **#EXT-X-BYTERANGE:** - Medya Segmentinin, URI tarafından tanımlanan kaynağın bir alt aralığı olduğunu belirtir.
- **#EXT-X-DISCONTINUITY** - Önceki ve sonraki medya bölümleri arasındaki süreksizliği gösterir.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Aynı Değişken Akışın veya farklı Değişken Akışların farklı yorumlamaları arasında senkronizasyona izin verir.
- **#EXT-X-KEY:** - Ortam Segmentlerinin şifresinin nasıl çözüleceğini belirtir.
- **#EXT-X-MAP:** - Ortam Başlatma Bölümünün nasıl elde edileceğini belirtir. Geçerli Medya Segmentlerini ayrıştırmak gerekir.
- **#EXT-X-PROGRAM-DATE-TIME:** - Medya Segmentinin ilk örneğini mutlak bir tarih ve/veya saatle ilişkilendirir.
- **#EXT-X-DATERANGE:** - Bir Veri Aralığı ilişkilendirir.
- **#EXT-XI-FRAMES-ONLY** - Oynatma Listesindeki her Medya Segmentinin tek bir I-karesini tanımladığını gösterir.
- **EXT-XI-FRAME-STREAM-INF** - Çalma listesi dosyasının Multimedya sunumunun I-karelerini içerdiğini gösterir.
- **#EXT-X-SESSION-DATA:** - İsteğe bağlı oturum verilerinin
bir Ana Çalma Listesinde taşınır.
- **#EXT-X-SESSION-KEY:** - Şifreleme anahtarlarına izin verir. İstemci, önce oynatma listesini okumadan bu anahtarları önceden yükleyebilir.
- **#EXT-X-ENDLIST** - Dosyaya daha fazla Medya Segmenti eklenmeyeceğini belirtir.

M3U tarafından kullanılan İnternet ortam türlerinin listesi aşağıdadır:

- **application/vnd.apple.mpegurl**: M3U için HLS uygulamalarındaki oynatma listelerine atıfta bulunmak için kullanılan tek kayıtlı ortam türüdür (2009'da tescil edilmiştir).
- Aşağıdaki İnternet ortamı türleri, HLS dışı uygulamalar tarafından kullanılır.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U Örneği ##

Bu, M3U dosyasının bir örneğidir.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referanslar ##

- [M3U - Vikipedi](https://en.wikipedia.org/wiki/M3U)
- [HTTP Canlı Akışı](https://tools.ietf.org/html/rfc8216)

