---
date: 2022-01-06
keywords: vtt, .vtt, vtt dosya formatı, .vtt dosya formatı, .vtt uzantısı, vtt uzantısı
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: ".vtt dosyası ve VTT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: VTT Dosya Biçimi - Web Video Metin İzleri Dosyası
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## .vtt dosyası nedir?

Bir VTT dosyası, Web Video Metin İzleri (WebVTT) formatını kullanarak zamanlanmış metin parçalarını (altyazılar veya resim yazıları gibi) görüntülemek için bilgi içeren bir metin dosyasıdır. Zamanlanmış metin parçaları, alt yazılar veya resim yazıları gibi bilgileri içerir. VTT dosyasının amacı, bir dosyaya metin bindirmeleri eklemektir.<video> . Biçim, SRT dosyalarına biraz benzer. WebVTT tabanlı metin dosyaları UTF-8 kullanılarak kodlanmıştır. Bir VTT dosyası, altyazılar, açıklamalar, altyazılar, açıklamalar, bölümler ve meta veriler gibi bilgileri içerir. Düz metin dosyaları olan VTT dosyaları, Microsoft Notepad, Apple TextEdit ve Notepad++ gibi metin düzenleyicileri kullanılarak açılabilir.

## VTT Dosya Biçimi - Daha fazla bilgi

VTT dosyaları, sıralı metin parçaları bilgilerini kaydetmek için WebVTT dosya formatını kullanır. Her zamanlanmış metin izi, aşağıdaki örnekte gösterildiği gibi "işaret" olarak da bilinen tek bir satırdan veya birden çok satırdan oluşur.

### VTT Dosyası Örneği

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT Dosya Yapısı

Bir VTT dosyasının yapı gereksinimleri aşağıdadır.

* İsteğe bağlı bir bayt sıralama işareti (BOM).
* "WEBVTT" dizisi.
* WEBVTT'nin sağında isteğe bağlı bir metin başlığı.
* Ardışık iki yeni satıra eşdeğer boş bir satır.
* Sıfır veya daha fazla ipucu veya yorum.
* Sıfır veya daha fazla boş satır.

## Referanslar

* [VTT - W3 Okulları](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

