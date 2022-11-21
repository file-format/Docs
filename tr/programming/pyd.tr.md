---
date: 2022-05-09
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD Dosya Formatı - Python Dinamik Modülü
linktitle: PYD
description: "PYD dosya formatı ve PYD dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .pyd dosyası nedir?

Bir PYD dosyası, çalışma zamanında diğer Python kodları tarafından çalıştırılabilen, Python'da yazılmış bir dinamik bağlantı kitaplığıdır. Kodun yeniden kullanımını kolaylaştıran ve uygulama yazmak için modül mimarisi sağlayan bir veya daha fazla Python modülü içerir. PYD dosyaları, örneğin helloworld.pyd gibi .pyd uzantılı oluşturulabilir ve kaydedilebilir. Uygulama geliştiriciler, uygulamalarına PYD modüllerini dahil etmek için import deyimini kullanabilirler. PYD dosyaları, Windows, Mac ve Linux işletim sistemi için kullanılabilen Python Software Foundation Python ile açılabilir.

## PYD Dosya Biçimi - Daha Fazla Bilgi

PYD dosyaları Python programlama dilinde yazılır ve Python kodu derlenerek oluşturulur.

## PY ve PYD Dosya Biçimleri Arasındaki Fark

Bir [PY](/tr/programming/py/) dosyası, olduğu gibi yürütülen ve diğer Python uygulamalarında yeniden kullanılabilir bir kod olarak eklenemeyen kaynak kodu içerir. Ancak, bir PYD dosyası, Windows işletim sisteminde kullanılmak üzere dinamik olarak bağlantılı bir kitaplıktır.

## PYD Dosyası Nasıl Oluşturulur?

Örneğin exmaple.pyd adlı bir modül oluşturularak bir PYD dosyası oluşturulabilir. Bu modül, örneğin PyMod_example() gibi bir veya daha fazla işlev biçimindeki tüm işlevleri içerecektir. Program bu kütüphaneyi dahil edip çağırdığında, modülü içe aktararak yapılabilir ve PyMod_example() işlevi çalışır.

## Referanslar ##

* [C/C++'da Python Uzantıları Oluşturma](https://sebsauvage.net/python/mingw.html)
* [Python (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

