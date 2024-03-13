---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML Fayl Formasıat
linktitle: TOML
description: LTOML fayl formatı və TOML faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## TOML faylı nədir? ##

TOML (Tom's Obvious Minimal Language) .toml uzantısından istifadə edən minimal konfiqurasiya fayl formatıdır. TOML asan oxunmaq, lüğətlərə birmənalı şəkildə xəritə vermək və müxtəlif məlumat strukturlarına asanlıqla təhlil etmək məqsədi daşıyır. TOML icma töhfələrini qəbul edən açıq mənbə spesifikasiyasına malikdir. TOML C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift və s. kimi bir çox proqramlaşdırma dilləri tərəfindən dəstəklənir. TOML faylları üçün MIME növü *application/toml*-dır.


## TOML Fayl Formatı ##

TOML faylları əsasən açar/dəyər Cütlükləri, bölmələr/cədvəllər, şərhlərdən ibarətdir və etibarlı UTF-8 kodlu Unicode sənədi olmalıdır. TOML String, Integer, Float, Boolean, Datetime, Massiv və Cədvəl (hesh cədvəli/lüğət) məlumat növlərini dəstəkləyir. TOML hərflərə həssas bir dildir.

### Sintaksis ###

- **Açar-dəyər cütləri**: Açar-dəyər cütləri bərabər işarəsi (=) ilə ayrılır. Hər bir cüt yeni sətirdə olmalıdır.

```toml
birinci = Tom
sonuncu = Preston-Verner
```

- **Şərhlər**: Şərhlər hash (#) simvolu ilə başlayır.

```toml
# Bu TOML sənədidir.
```

- **Strlər**: Sətirlər dırnaq () işarələri ilə əhatə olunub.

```toml
string = Nümunə sətir
```

- **Çoxxətli Sətirlər**: Çoxsətirli Sətirlər üç dırnaq () işarəsi ilə əhatə olunub.

```toml
[ev ünvanı]
küçə = 123 Tornado Xiyabanı
Suite 16
şəhər = Şərq Centerville
dövlət = KS
```

- **Tam ədədlər/Floats**

```toml
tam = 20
float = 20.5
```

- **Booleans**: Booleans həmişə kiçik hərfdir.

```toml
bool1 = doğrudur
bool2 = yalan
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

```toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
yerli_tarix = 1979-05-27
yerli vaxt = 07:32:00
```

- **Masivlər**: Massivlər elementləri vergül (,) ilə ayrılmış kvadrat mötərizələrlə əhatə olunub.

```toml
rənglər = [ qırmızı, sarı, yaşıl ]
```

- **Cədvəllər**: Cədvəllər kvadrat mötərizə ([]) ilə əhatə olunmuş yeni sətirdə başlıqlarla müəyyən edilən açar/dəyər cütlərinin toplusudur. Cədvəl yeni başlıq təqdim edildikdə və ya fayl bitdikdə bitir.

```toml
[ev ünvanı]
küçə = 123 Tornado Xiyabanı
Suite 16
şəhər = Şərq Centerville
dövlət = KS

[ofis ünvanı]
küçə = 123 Tornado Xiyabanı
Suite 16
şəhər = Şərq Centerville
dövlət = KS
```

Sətirli cədvəllər hər bir açar/dəyər cütü vergül (,) ilə ayrılmış əyri mötərizələrlə ({}) əhatə olunmuşdur.

```toml
ad = {ilk = Tom, sonuncu = Pitt}
```

## İstinadlar ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

