{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Malzeme Değişim Formatı",
  "keywords" :[ "MXF", "matroska video", "mkv formatı", "MXF dosyalarının nasıl oynatılacağı", "SMPTE", "multimedya", "video"],
  "description":"MXF dosya formatı ve MXF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## MXF Dosyası Nedir?

.mxf uzantılı bir dosya, dosyayla ilgili meta veri bilgileriyle birlikte dijital video ve ses ortamını içeren bir multimedya taşıyıcı biçimidir. Medya ve eğlence endüstrisinde çalışan mühendislik, teknoloji ve yöneticilerden oluşan küresel bir dernek olan SMPTE (Sinema Filmi ve Televizyon Mühendisleri Derneği) standardını takip eder. MXF dosyaları, [AVI](/tr/video/avi/) veya [MOV](/tr/video/mov/) gibi diğer dosya biçimlerine dönüştürülebilir.

## MXF Dosya Biçimi

MXF dosyaları aslında belirli bir biçimde bir bayt dizisinden oluşan ikili dosyalardır. Kod çözme uygulamaları, onu anlamak ve ondan bilgi çıkarmak için bu formatla uyumlu olmalıdır. Biçim, aşağıda açıklanan KLV kodlamasını kullanarak geriye dönük uyumluluğu bozmadan yeni öğeler eklenmesine izin verir.

* Anahtar – öğenin tanımlayıcısı, bir SMPTE Evrensel Etiketi (UL)
* Uzunluk – bu öğe için gereken alan miktarını azaltmak için kullanılan değişken uzunluklu kodlama olan verinin uzunluğu
* Değer – öğenin gerçek değeri.

### SMPTE Biçim Özellikleri

MXF dosya biçimi, aşağıdaki SMPTE belirtimleriyle tanımlanmıştır.

* SMPTE ST 377-1:2011. Televizyon — Malzeme Değiştirme Biçimi (MXF) — Dosya Biçimi Spesifikasyonu
* SMPTE ST 377-2 (Ocak 2012 itibariyle devam eden çalışmalar). MXF için KLV Kodlu Uzantı Söz Dizimi.
* SMPTE ST 378:2004 (Arşivlenmiş 2010). Televizyon — Malzeme Değiştirme Formatı (MXF) — Çalışma Modeli 1a (Tek Ürün, Tek Paket)
* SMPTE ST 379-1:2009. Malzeme Değiştirme Biçimi (MXF) — MXF Genel Kapsayıcısı
* SMPTE ST 379-2:2010. Malzeme Değişim Formatı (MXF) -- MXF Kısıtlı Genel Konteyner
* SMPTE ST 380:2004. Televizyon — Malzeme Değişim Formatı (MXF) — Açıklayıcı Meta Veri Şeması-1 (Standart, Dinamik)
* SMPTE ST 381-1:2005. Televizyon — Malzeme Değişim Formatı (MXF) — MPEG Akışlarını MXF Genel Kapsayıcısına (Dinamik) Eşleme
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — MPEG Akışlarını MXF Kısıtlı Genel Kapsayıcıya Eşleme
* SMPTE ST 382:2007. Material Exchange Format (MXF) — AES3 Akışlarını ve Yayın Dalgası Sesini MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 383:2008. Televizyon — Malzeme Değişim Formatı (MXF) — DV-DIF Verilerini MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 384:2005. Televizyon — Malzeme Değişim Formatı (MXF) — Sıkıştırılmamış Resimlerin MXF Genel Kapsayıcısına Eşleştirilmesi
* SMPTE ST 385:2004. Televizyon — Malzeme Değişim Formatı (MXF) — SDTI-CP Essence ve Meta Verilerini MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 386:2004 (Arşivlenmiş 2010). Televizyon — Malzeme Değişim Formatı (MXF) — Tip D-10 Essence Verilerini MXF Genel Kabına Eşleme
* SMPTE ST 387:2004 (Arşivlenmiş 2010). Televizyon — Malzeme Değişim Formatı (MXF) — Tip D-11 Essence Verilerini MXF Genel Kabına Eşleme
* SMPTE ST 388:2004 (Arşivlenmiş 2010). Televizyon — Malzeme Değişim Formatı (MXF) — A Yasası Kodlu Sesi MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 389:2005. Televizyon — Malzeme Değiştirme Formatı (MXF) — MXF Genel Konteyner Ters Oynatma Sistemi Öğesi
* SMPTE ST 390:2011. Televizyon — Malzeme Değişim Formatı (MXF) — Özel İşlem Modeli "Atom" (Tek Bir Öğenin Basitleştirilmiş Temsili)
* SMPTE ST 391:2004 (Arşivlenmiş 2010). Televizyon — Malzeme Değiştirme Formatı (MXF) — Operasyonel Model 1b (Tek Öğe, Birleşik Paketler)
* SMPTE ST 392:2004. Televizyon — Malzeme Değişim Formatı (MXF) — Operasyonel Model 2a (Çalma Listesi Öğeleri, Tekli Paket)
* SMPTE ST 393:2004. Televizyon — Malzeme Değişim Formatı (MXF) — Operasyonel Model 2b (Çalma Listesi Öğeleri, Birleşik Paketler)
* SMPTE ST 394:2006. Televizyon — Malzeme Değişim Formatı (MXF) — MXF Genel Kapsayıcısı için Sistem Şeması 1
* SMPTE ST 405:2006. Televizyon — Malzeme Değişim Formatı (MXF) — MXF Genel Konteyner Sistemi Şeması 1 için Öğeler ve Bireysel Veri Öğeleri
* SMPTE ST 407:2006. Televizyon — MXF — Çalışma Modelleri 3a ve 3b
* SMPTE ST 408:2006. Televizyon — MXF — Çalışma Modelleri 1c, 2c ve 3c
* SMPTE ST 410: 2008. Malzeme Değişim Formatı - Genel Akış Bölümü.
* SMPTE ST 422:2006. Malzeme Değişim Formatı — JPEG2000 Kod Akışlarını MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 429.4:2006. D-Sinema Ambalajı — MXF JPEG 2000 Uygulaması
* SMPTE ST 429.5:2006. D-Cinema Paketleme — Zamanlı Metin İzleme Dosyası
* SMPTE ST 429.6:2006. D-Cinema Paketleme — MXF İzleme Dosyası Özü Şifrelemesi
* SMPTE ST 434:2006. Malzeme Değişim Formatı — Meta Veriler ve Dosya Yapısı Bilgileri için XML Kodlaması
* SMPTE ST 436:2006. Televizyon — VBI Hatları ve Yardımcı Veri Paketleri için MXF Eşlemeleri
* SMPTE ST 2019-4:2009. VC-3 Kodlama Birimlerini MXF Genel Kapsayıcısına Eşleme
* SMPTE ST 2037:2009. VC-1'i MXF Genel Kapsayıcısına Eşleme
* SMPTE RP 2008:2008. Malzeme Değişim Formatı — AVC Akışlarını MXF Genel Kapsayıcısına Eşleme
* SMPTE RP 2057:2011. MXF'de Metin Tabanlı Meta Veri Taşıma
* SMPTE EG 41:2004. Malzeme Değişim Formatı (MXF) — Mühendislik Yönergesi. Not: Bu belge, Ocak 2012'de başvurulduğunda SMPTE Web sitesinde artık listelenmiyordu.
* SMPTE EG 42:2004. Malzeme Değişim Formatı (MXF) — MXF Açıklayıcı Meta Verileri
* SMPTE RDD 3:2008. e-VTR MXF Birlikte Çalışabilirlik Spesifikasyonu
* SMPTE RDD 9-2009. Sony MPEG Uzun GOP Ürünlerinin MXF Birlikte Çalışabilirlik Spesifikasyonu
* SMPTE meta veri kayıt tablosu menüsü.

### MXF Yapısal Meta Verileri

Yapısal meta veriler, dosyanın içeriği hakkında yararlı bilgiler içerdiğinden bir MXF dosyasında esastır. MXF meta verileri kare hızı, kare boyutu, dosya oluşturma tarihi ve özel değişiklik tarihi gibi bilgileri içerir. Yapısal meta veriler, çeşitli temel bileşenleri teknik olarak tanımlamayı ve çıktı zaman çizelgesinin nasıl oluşturulduğunu aktarmayı içeren bir MXF dosyasının yapısını ve yeteneklerini açıklar.

## Referanslar

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - İlerleme Raporu](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [MXF için OpenSource C++ Kitaplığı](http://www.freemxf.org/)

