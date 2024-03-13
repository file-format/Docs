---
date: 2019-10-11
keywords: py, python, .py, py file format, how to open py file, how to run py files, how to run python files, how to run python
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY Fayl Formasıat
linktitle: PY
description: LPY faylı yarada və aça bilən PY fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## PY faylı nədir? ##

.py uzantılı Fayllar Python mənbə kodunu ehtiva edir. Python dili bu gün çox məşhur bir dilə çevrilib. Sistem skriptləri, veb və proqram təminatının inkişafı və riyaziyyat üçün istifadə edilə bilər. Python platformalararası uyğunluğu dəstəkləyir; o deməkdir ki, Python-da hazırlanmış proqramlar Windows, MAC, Linux, Raspberry Pi və s. kimi müxtəlif platformalarda işləyə bilər. Python ingilis dilinə bənzər sadə və asan oxunan sintaksisi təmin edir. Tərtibatçılar bir neçə sətir Python kodu yazaraq ağlabatan proqram təminatı yaza bilərlər. Python tərcüməçi sistemində işlədiyi üçün kod yazılan kimi icra oluna bilər ki, bu da onu prototipləmə üçün çox yaxşı edir.

## Qısa tarix ##

Python was conceived in the late 1980s by Guido van Rossum as a successor to ABC programming language. Its implementation began in December 1989 with Van Rossum as the sole lead developer. He worked on python until 12 July 2018. 2019-cu ilin yanvar ayında aktiv Python əsas tərtibatçıları layihəyə rəhbərlik etmək üçün Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw və Van Rossumdan ibarət beş üzvdən ibarət Rusiya İdarəetmə Şurası seçdilər.

### Versiyalar ###

- Python 2.0 16 oktyabr 2000-ci ildə buraxıldı.
- Python 3.0 3 dekabr 2008-ci ildə buraxıldı.

## py faylını necə işlətmək olar ##

Quraşdırılmış Python versiyasını yoxlamaq üçün aşağıdakı əmrdən istifadə edə bilərsiniz:

```cmd
python --version
```

Bu, versiyanı konsolda çıxaracaq

```cmd
Python 3.7.4
```

Python maşınınızda quraşdırılmayıbsa, siz [python.org](https://www.python.org/) səhifəsinə keçib müvafiq əməliyyat sisteminiz üçün Python-u endirib quraşdıra bilərsiniz.

Python skriptini yerinə yetirmək üçün aşağıdakı əmrdən istifadə edə bilərsiniz:

```cmd
python helloworld.py
```

*helloworld.py* aşağıdakı kodu ehtiva edən skript faylıdır

```py
print("Hello World from Python")
```

Bu, konsol pəncərəsində aşağıdakıları çap edəcək.

```cmd
Hello World from Python
```

Qeyd: IDE-lərdən istifadə edirsinizsə, onlar Python-u işə salmaq üçün ekranda düymələr və ya müxtəlif klaviatura qısa yollarını təmin edirlər. Məsələn, Python skriptini yerinə yetirməyə imkan verən PyCharm-da redaktoru olan tıxacda oynatma düyməsi göstərilir.

## PY Fayl Format ##

Python oxunaqlılıq üçün nəzərdə tutulmuşdur və ingilis və riyaziyyat dillərinə oxşarlıqlara malikdir. Python, digər dillərdə istifadə olunan nöqtəli vergül və ya mötərizədən fərqli olaraq, tam əmri göstərmək üçün yeni sətirlərdən istifadə edir. Əhatə dairələri, döngələr və funksiyalar üçün Python digər dillərdə istifadə olunan əyri mötərizələrdən fərqli olaraq girinti və boşluqlara əsaslanır.

### Sintaksis ###

Aşağıda Python sintaksisinin bir nümunəsidir.

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

## İstinadlar ##

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

