---
date: 2022-03-20
keywords: mxl, Musepack dosya formatı, .mxl uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "MXL dosya formatı ve MXL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: MXL Dosya Formatı - Sıkıştırılmış MusicXML Dosyası
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## MXL dosyası nedir?

Bir MXL dosyası, dijital notalar alışverişi için açık standart bir format olan MusicXML dosya formatının sıkıştırılmış şeklidir. Düz metin MusicXML dosyalarının boyutu büyüktür ve bu tür dosyaların bir sayfa dağıtım formatı olarak kullanımı, büyük dosya boyutundan etkilenmiştir. Bu sorunlar [MusicXML](https://www.musicxml.com/) 2.0 ile, dosyaları orijinal MIDI dosyalarına benzer dosya boyutunu küçültmeye yetecek kadar sıkıştıran MXL dosya formatı tanıtılarak ele alındı. MXL dosyaları için önerilen ortam türü application/vnd.recordare.musicxml'dir.

## MXL Dosya Biçimi

MXL dosyaları, .mxl dosya uzantılı [ZIP](/tr/compression/zip/) sıkıştırılmış [XML](/tr/web/xml/) dosyaları olarak saklanır. MXL dosyaları, [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)'de belirtildiği gibi DEFLATE algoritmasıyla sıkıştırılır.

### MXL Dosya Yapısı

Her MXL dosyası, dosyanın MusicXML sürümünün başlangıç noktasını açıklayan bir META-INF/container.xml dosyasına sahip olması gereken ZIP tabanlı bir XML formatına sahiptir. MXL dosya formatı için tanımlanmış karşılık gelen bir .xsd dosyası yok.

Basit bir container.xml dosyasının içeriği aşağıdaki gibidir. Bu örnek, MakeMusic web sitesinde bulunan Dichterliebe01.mxl dosyasından alınmıştır.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Bu örnekte,<container> eleman belge elemanıdır. bu<rootfiles> eleman bir veya daha fazla içerebilir<rootfile> elemanlar, ilk<rootfile> MusicXML kökünü açıklayan öğe. olarak kullanılan bir MusicXML dosyası<rootfile> sahip olabilir<score-partwise> ,<score-timewise> , veya<opus> belge öğesi olarak.

## Referanslar

* [Sıkıştırılmış MXL Dosyaları](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

