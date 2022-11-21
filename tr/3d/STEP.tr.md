---
date: 2019-10-11
keywords: step, .step, step dosya formatı, step dosyaları nasıl açılır, .step uzantısı, step uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ADIM Dosya Biçimi
linktitle: STEP
description: "STEP dosya formatı ve STEP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Bir ADIM dosyası nedir?

STEP dosyası, Bilgisayar destekli tasarım (CAD) için yaygın olarak kullanılan bir veri değişim formatıdır. 1994 yılında ISO komitesi tarafından "ISO 10303-21" adı altında standardize edilmiştir. ISO 10303-21, EXPRESS veri modelleme dilinde verileri temsil etmek için kodlama mekanizmasını tanımlar. Bir STEP- dosyası, p21-Dosyası ve STEP Fiziksel Dosyası olarak da bilinir. STEP dosyası için kullanılan dosya uzantıları .stp ve .step'dir.

## Temel Tarih

1994 yılında, orijinal Bölüm 21 spesifikasyonu yayınlandı. 1996'da yayınlanan teknik düzeltme ile düzeltilen bazı hatalar var. İkinci baskı, düzeltmeyi ve çeşitli veri bölümleri için uzantıları içeren 2002'de yayınlandı. Varlıkların ve değerlerin harici dosyalarda depolanmasına izin veren bağlantı ve referans bölümleri ekleyen üçüncü sürüm 2016'da yayınlandı. Dizilere UTF-8 desteği eklendi. Dosyanın içeriğini doğrulamak ve kimlik bilgilerini doğrulamak için dijital imzalar eklendi. ZIP kullanarak değişim yapısını sıkıştırma ve depolama desteği de eklendi.

## ADIM Dosya Biçimi

Bir STEP dosyası için düz metin formatı, bir dizi kayıttan oluşur. Karakter seti, ISO 10646'nın kod noktaları olarak tanımlanır. "ISO-10303-21;" ilk kayıttaki ilk karakterlerdir. Yorumlar "/*" ve "*/" karakterleri ile çevrilidir. Son kayıt "END-ISO-10303-21;" içerir. STEP dosyası 2002 versiyonuna uygunsa. 2016 versiyonuna uygun olması durumunda "END-ISO-10303-21;" den sonra bir veya birden fazla dijital imza olabilir; terminatör. Satır sonları "\N\" ile, sayfa sonları ise "\F\" ile gösterilir.

STEP dosyası bölümlere ayrılmıştır ve adları saklı terimlerdir. Tüm bölümler "ENDSEC" kaydı ile sona erer ve aşağıda gösterilen sırada olmalıdır.

- **HEADER**: Bu zorunlu ve tekrar edilemez bir bölümdür. Aşağıdaki varlıklardan oluşur:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ÇAPA**: 2016 sürümünde sunulan, isteğe bağlı, tekrarlanmayan bir bölümdür. Başvurulabilmeleri için örnekler için harici adları tanımlar.
- **REFERANS**: 2016 sürümünde de sunulan, isteğe bağlı, tekrarlanmayan bir bölümdür. Bu bölümdeki her giriş, bir giriş/değer örnek adını harici bir dosyadaki bir örnek/değerle ilişkilendirir.
- **VERİ**: Model örneğinin temel içeriğini içeren, isteğe bağlı tekrarlanabilir bir bölümdür.
- **İMZA**: 2016 sürümünde sunulan, isteğe bağlı tekrarlanabilir bir bölümdür. Dosyanın içeriğini doğrulamak veya kimlik bilgilerini doğrulamak için dijital imzayı tutar.

## Referanslar

- [ISO 10303-21 - Vikipedi](https://en.wikipedia.org/wiki/ISO_10303-21)

