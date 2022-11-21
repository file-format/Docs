---
date: 2019-10-11
keywords: WEBM, WEBM dosyası nedir, WEBM Dosya Biçimi
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "WEBM dosya formatı ve WEBM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
title: WEBM - WebM Video Dosyası Biçimi
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## WEBM dosyası nedir?

.webm uzantılı bir dosya, açık, telifsiz WebM dosya biçimini temel alan bir video dosyasıdır. Web üzerinde video paylaşımı için tasarlanmıştır ve video ve ses formatlarını içeren dosya kapsayıcı yapısını tanımlar. WebM %100 ücretsizdir ve HTML, HTTP ve TCP/IP gibi herkesin uygulamaya açık olduğu açık teknolojileri temel alan yüksek kaliteli uygulama sunar. WebM, web'de video sunmak için özel olarak tasarlanmıştır, bu da onu düşük hesaplama ayak iziyle akış için optimize eder. Bu, özellikle düşük güçlü netbook'lar, el bilgisayarları ve tabletler gibi herhangi bir cihazda video oynatımı için uygun hale getirir.

## WEBM Dosya Biçimi

WebM dosya yapısı, Matroska [MKV](/tr/video/mkv/) kapsayıcı dosya biçiminin bir alt kümesini temel alır. Bir WebM dosyasında bulunan video akışları, sıkıştırmada oldukça verimli olan VP8 veya VP9 sıkıştırma teknolojileri kullanılarak sıkıştırılır. Benzer şekilde, bir WebM dosyasındaki ses akışları, [Xiph Foundation](https://www.xiph.org/) tarafından geliştirilen Vorbis veya Opus codec'leri kullanılarak sıkıştırılır. Tüm bu videolar ve ses codec'leri telifsizdir ve herhangi bir ücret ödemeden kullanılabilir.

WebM dosya formatı için özetlenmiş özellikler aşağıdadır.

|Alan|Açıklama|
---|---|
|MIME tipi |video/webm|
|Yalnızca ses MIME türü |ses/webm|
|Üniforma Tipi Tanımlayıcı| org.webmproject.webm|
|Video Codec Adı| VP8 veya VP9|
|Ses Codec Adı| Vorbis veya Opus|

### WebM Öğeleri

Matroska belirtimlerinin bir alt kümesi olan WebM, Matroska işlevlerinden bazıları için destek sağlar. Desteklenen öğelerin açıklaması aşağıdadır.

#### EBML

|Ad |Açıklama|
---|---|
|EBML|İzlenecek verilerin EBML özelliklerini ayarlayın. Her EBML belgesi bununla başlamalıdır.|
|EBMLVersion |Dosyayı oluşturmak için kullanılan EBML ayrıştırıcısının sürümü.|
|EBMLReadVersion|Ayrıştırıcının bu dosyayı okumak için desteklemesi gereken minimum EBML sürümü.|
|EBMLMaxIDLength |Bu dosyada bulacağınız kimliklerin maksimum uzunluğu (Matroska'da 4 veya daha az).|
|EBMLMaxSizeLength|Bu dosyada bulacağınız boyutların maksimum uzunluğu (Matroska'da 8 veya daha az). Bu, bir öğenin başında belirtilen öğe boyutunu geçersiz kılmaz. EBMMLMaxSizeLength tarafından izin verilenden daha büyük belirtilen bir boyuta sahip öğeler geçersiz kabul edilecektir.|
|DocType|Bu EBML başlığını izleyen belge türünü açıklayan bir dize (bizim durumumuzda "webm").|
|DocTypeVersion|Dosyayı oluşturmak için kullanılan DocType yorumlayıcısının sürümü.|
|DocTypeReadVersion|Bir yorumlayıcının bu dosyayı okumak için desteklemesi gereken minimum DocType sürümü.|

#### Küresel Unsurlar

Şu anda, hasarlı veriler kullanılırken beklenmeyen davranışlardan kaçınmak amacıyla, yalnızca hasarlı verileri geçersiz kılmak için kullanılan "Void" öğesi desteklenmektedir. İçerik atılır. Daha sonra kullanmak üzere bir alt öğede yer ayırmak için de kullanılır.

#### Segment
Bu öğe, diğer tüm üst düzey (seviye 1) öğeleri içerir. Tipik olarak bir Matroska dosyası 1 bölümden oluşur.

#### Meta Arama Bilgisi

Aşağıdaki arama bilgileri desteklenmektedir.

|Öğe Adı |Açıklama|
---|---|
|SeekHead |Başka bir 1. düzey öğenin konumunu içerir.|
|Seek |Bir EBML öğesi için tek bir arama girişi içerir.|
|SeekID |Öğe adına karşılık gelen ikili kimlik.|
|SeekPosition |Elemanın segmentteki sekizli cinsinden konumu (0 = birinci düzey 1 öğe).|

## Referanslar

* [WebM](https://www.webmproject.org/)
* [WebM Kod Depoları](https://www.webmproject.org/code/#webp-repositories)

