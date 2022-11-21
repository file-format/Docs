---
date: 2019-10-11
keywords: py, python, .py, py dosya formatı, py dosyası nasıl açılır, py dosyaları nasıl çalıştırılır, python dosyaları nasıl çalıştırılır, python nasıl çalıştırılır
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY Dosya Biçimi
linktitle: PY
description: "PY dosya formatı ve PY dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## .py dosyası nedir? ##

.py uzantılı dosyalar Python kaynak kodunu içerir. Python dili günümüzde çok ünlü bir dil haline geldi. Sistem komut dosyası oluşturma, web ve yazılım geliştirme ve matematik için kullanılabilir. Python, platformlar arası uyumluluğu destekler; Python'da geliştirilen uygulamaların Windows, MAC, Linux, Raspberry Pi vb. farklı platformlarda çalışabileceği anlamına gelir. Python, İngilizce'ye benzer basit ve okunması kolay bir sözdizimi sağlar. Geliştiriciler, birkaç satır Python kodu yazarak makul bir yazılım uygulaması yazabilirler. Python bir tercüman sistemi üzerinde çalıştığından, kod yazılır yazılmaz çalıştırılabilir, bu da onu prototipleme için çok iyi kılar.

## Kısa Tarih ##

Python, 1980'lerin sonunda Guido van Rossum tarafından ABC programlama dilinin halefi olarak tasarlandı. Uygulaması Aralık 1989'da Van Rossum'un tek lider geliştirici olmasıyla başladı. 12 Temmuz 2018'e kadar python üzerinde çalıştı. Ocak 2019'da aktif Python çekirdek geliştiricileri, projeye liderlik etmesi için Nick Coghlan, Brett Cannon, Carol Willing, Barry Varşova ve Van Rossum'dan oluşan beş üyeli bir "Yönlendirme Konseyi" seçti.

### Sürümler ###

- Python 2.0, 16 Ekim 2000'de yayınlandı.
- Python 3.0, 3 Aralık 2008'de yayınlandı.

## py dosyası ## nasıl çalıştırılır

Yüklü Python sürümünü kontrol etmek için aşağıdaki komutu kullanabilirsiniz:

```cmd
python --version
```

Bu, konsoldaki sürümü şu şekilde çıkaracaktır:

```cmd
Python 3.7.4
```

Makinenizde Python yüklü değilse, [python.org](https://www.python.org/) adresine giderek ilgili işletim sisteminiz için Python'u indirip yükleyebilirsiniz.

Bir Python betiğini çalıştırmak için aşağıdaki komutu kullanabilirsiniz:

```cmd
python helloworld.py
```

*helloworld.py*, aşağıdaki kodu içeren bir betik dosyasıdır

```py
print("Hello World from Python")
```

Bu, konsol penceresinde aşağıdakileri yazdıracaktır.

```cmd
Hello World from Python
```

Not: IDE'ler kullanıyorsanız, Python'u çalıştırmak için ekranda düğmeler veya farklı klavye kısayolları sağlarlar. Örneğin, PyCharm'da Python betiğini çalıştırmanıza izin veren düzenleyiciyle ciltte bir oynatma düğmesi gösterilir.

## PY Dosya Biçimi ##

Python okunabilirlik için tasarlanmıştır ve İngilizce ve Matematik ile benzerlikleri vardır. Python, diğer dillerde kullanılan noktalı virgül veya parantezin aksine tam komutu belirtmek için yeni satırlar kullanır. Kapsamlar, döngüler ve işlevler için Python, diğer dillerde kullanılan kaşlı ayraçların aksine girinti ve boşluklara güvenir.

### Sözdizimi ###

Aşağıda bir Python sözdizimi örneği verilmiştir.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Referanslar ##

- [Python (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

