---
date: 2020-11-11
keywords: myi, .myi, myi dosya formatı, myi dosyaları nasıl açılır, .myi uzantısı, myi uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI Dosya Biçimi
linktitle: MYI
description: "MYI dosya formatı ve MYI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## MYI Dosyası Nedir? ##

MYI, MySQL MyISAM İndeks dosyası olarak da bilinir. MySQL tarafından MyISAM tablosu için dizinleri depolamak için kullanılır. MySQL veritabanı dizini, tablonun yapısını tanımlar ve tabloların bütünlüğünü kontrol etmek için kontrol mekanizmasını içerir.

## MYI Dosya Biçimi ##

MYI dosyası, başlık ve anahtar değerler olmak üzere iki bölümden oluşur.

### MYI Başlığı ###

Başlık, seçenekler, dosya boyutları ve anahtarlar hakkında bilgi içerir. MySQL'deki anahtarlar aşağıdaki gibi bir komutla oluşturulur:

```sql
CREATE [UNIQUE] INDEX.
```

MYI dosyalarını okuyan ve yazan dosyalar ./myisam dizinindedir. Aşağıdaki dosyalara sahiptir:

- mi_open.c: Bu dosya, başlığın her bir bölümünü yazan rutinleri içerir.
- mi_create.c: Bu dosya, mi_open.c yordamlarını çağıran yordamlara sahiptir.
- myisamdef.h: Bu dosya yapı tanımlarına sahiptir.

Başlık aşağıdaki bölümleri içerir:

- durum: Durum, mi_open.c, mi_state_info_write() tarafından yazılır. Bu yapı dosyada bir kez oluşur.
- temel: Temel, mi_open.c, mi_base_info_write() tarafından yazılır. MI_BASE_INFO, myisamdef.h içindeki tabana karşılık gelen yapıdır. Bu yapı dosyada bir kez oluşur.
- keydef: keydef, mi_open.c, mi_keydef_write() tarafından yazılır. MI_KEYDEF, myisamdef.h'deki keydef'e karşılık gelen yapıdır. Her dizin için görünen çok oluşumlu bir yapıdır.
- recinfo: recinfo, mi_open.c, mi_recinfo_write() tarafından yazılır. MI_COLUMNDEF, myisamdef.h içindeki recinfo için karşılık gelen yapıdır. Bir anahtarda görünen her alandan bir kez görünen çoklu oluşum yapısıdır.

### Anahtar değerler ###

MySQL'deki sayfalara blok denir. Anahtar değerler bloklar halindedir. Bir blok yalnızca bir dizinden bilgi içerir. Her anahtar, tüm sütunların tüm içeriğini içerir. Normal blok uzunluğu 0x0400 (1024) bayttır. İşaretçi, bir sıralı satır numarası içeren sabit satırlı tablolar için sabit boyutlu (4 bayt) bir numaraya sahiptir. Anahtar boşsa, bayt 0x00'dür. Normal bir blok en az %65 doludur ve tipik olarak %80 doludur.

myisamdef.h dosyası, sabitlerle ifade edilen aşağıdaki bilgileri içerir. Maksimum anahtar sayısı 32'dir (MI_MAX_KEY) ve bir anahtardaki maksimum segment sayısı 16'dır (MI_MAX_KEY_SEG). Anahtarın maksimum uzunluğu 500'dür (MI_MAX_KEY_LENGTH). Bloğun maksimum uzunluğu 16384'tür (MI_MAX_KEY_BLOCK_LENGTH).

## Referanslar ##

- [.MYI Dosyası](https://dev.mysql.com/doc/dev/mysql-server/latest/)

