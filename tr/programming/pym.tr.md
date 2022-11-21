---
date: 2022-05-09
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM Dosya Biçimi - PYM Makro Önişlemci Dosyası
linktitle: PYM
description: "PYM dosya formatı ve PYM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .pym dosyası nedir?

Bir PYM dosyası, Python programlama dilini temel alan bir makro önişlemci dosyasıdır. VRVis Research tarafından geliştirilmiştir ve makro kısayollarını saklar. PYM dosyası, Python yorumlayıcısının ön işleme aşaması tarafından yorumlandığında, bu kısayollar tam metinlerinin yerine geçecek şekilde genişletilir. Ek olarak, bir makro önişlemcisi tarafından gerçekleştirilebilen isteğe bağlı üçüncü bir işlem de dosya eklemedir. PYM dosyaları Linux'ta Notepad, Notepad++, Apple TextEdit ve VI gibi metin editörlerinde açılabilir.

## PYM Dosya Biçimi

PYM dosyaları, diske düz metin dosyaları olarak kaydedilir. Bir PYM dosyası, "#include" yönergesini kullanan diğer dosyaları da içerebilir.

### PYM Sözdizimi

PYM ifadeleri aşağıda gösterildiği gibi ""#begin python" ve "#end python" işaretçileri arasına dahil edilmiştir.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Makro Genişletme

PYM makro açılımı iki dizi ile temsil edilir, yani <[ ve ]>. Bunlar özel html etiketleridir ve bir satırın herhangi bir yerinde görünebilir. Küçük bir PYM örneği aşağıdaki gibidir.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Bunu PYM aracılığıyla çalıştırmanın çıktısı aşağıdaki gibidir:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referanslar ##

* [PYM - Python Tabanlı Bir Makro Ön İşlemci](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM Tercümanları](https://github.com/interpreters/pym)

