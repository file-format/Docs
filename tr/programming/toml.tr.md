---
date: 2019-10-11
keywords: toml, .toml, toml dosya formatı, toml dosyaları nasıl açılır, .toml uzantısı, toml uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML Dosya Biçimi
linktitle: TOML
description: "TOML dosya formatı ve TOML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## TOML dosyası nedir? ##

TOML (Tom's Obvious Minimal Language), .toml uzantısını kullanan minimal bir yapılandırma dosyası biçimidir. TOML, okunması kolay olmayı, sözlüklere açık bir şekilde eşlemeyi ve farklı veri yapılarına kolayca ayrıştırmayı amaçlar. TOML, topluluk katkıları alan bir açık kaynak belirtimine sahiptir. TOML, C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift vb. birçok programlama dili tarafından desteklenir. TOML dosyaları için MIME türü *application/toml* şeklindedir.


## TOML Dosya Biçimi ##

TOML dosyaları temel olarak anahtar/değer Çiftleri, bölümler/tablolar, yorumlardan oluşur ve geçerli bir UTF-8 kodlu Unicode belgesi olmalıdır. TOML, String, Integer, Float, Boolean, Datetime, Array ve Table(karma tablo/sözlük) veri türlerini destekler. TOML, büyük/küçük harfe duyarlı bir dildir.

### Sözdizimi ###

- **Anahtar/Değer Çiftleri**: Anahtar/değer çiftleri eşittir işaretiyle (=) ayrılır. Her çift yeni bir satırda olmalıdır.

```toml
ilk = "Tom"
son = "Preston-Werner"
```

- **Yorumlar**: Yorumlar kare (#) simgesiyle başlar.

```toml
# Bu bir TOML belgesidir.
```

- **Dizeler**: Dizeler tırnak (") içine alınır.

```toml
string = "Örnek Dizi"
```

- **Çok Satırlı Dizeler**: Çok Satırlı Dizeler üç tırnak (""") işaretiyle çevrilidir.

```toml
[Ev Adresi]
sokak = """123 Kasırga Yolu
Süit 16"""
şehir = "Doğu Centerville"
durum = "KS"
```

- **Tamsayılar/Kayanlar**

```toml
tamsayı = 20
kayan = 20.5
```

- **Boolean**: Boolean her zaman küçük harftir.

```toml
bool1 = doğru
bool2 = yanlış
```

- **Date-Time**: DateTime için aşağıdaki örnekte gösterildiği gibi RFC 3339 formatlı tarih-saat kullanabilirsiniz.

```toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
yerel_tarih = 1979-05-27
yerel_zaman = 07:32:00
```

- **Diziler**: Diziler, öğeleri virgülle (,) ayırarak köşeli parantezler içine alınır.

```toml
renkler = [ "kırmızı", "sarı", "yeşil" ]
```

- **Tablolar**: Tablolar, köşeli parantezler ([]) içine alınmış yeni bir satırdaki başlıklarla tanımlanan anahtar/değer çiftleri koleksiyonlarıdır. Tablo, yeni bir başlık sağlandığında veya dosya bittiğinde sona erer.

```toml
[Ev Adresi]
sokak = """123 Kasırga Yolu
Süit 16"""
şehir = "Doğu Centerville"
durum = "KS"

[Ofis adresi]
sokak = """123 Kasırga Yolu
Süit 16"""
şehir = "Doğu Centerville"
durum = "KS"
```

Satır içi tablolar, her bir anahtar/değer çiftinin virgülle (,) ayrıldığı kaşlı ayraçlar ({}) ile çevrilidir.

```toml
isim = {ilk = "Tom", son = "Pitt" }
```

## Referanslar ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

