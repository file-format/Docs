---
date: 2022-05-09
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Формат файла PYM — файл препроцессора макросов PYM
linktitle: PYM
description: "Узнайте о формате файлов PYM и API-интерфейсах, которые могут создавать и открывать файлы PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYM вариант №

Файл PYM представляет собой файл препроцессора макросов, основанный на языке программирования Python. Он был разработан VRVis Research и хранит ярлыки макросов. Когда файл PYM интерпретируется на этапе предварительной обработки интерпретатора Python, эти ярлыки раскрываются как замена их полного текста. Кроме того, третья необязательная операция, которую может выполнять препроцессор макросов, — включение файла. Файлы PYM можно открывать в текстовых редакторах, таких как Notepad, Notepad++, Apple TextEdit и VI в Linux.

## Формат файла PYM

Файлы PYM сохраняются как текстовые файлы на диск. Файл PYM также может включать другие файлы с помощью директивы #include.

### Синтаксис PYM

Операторы PYM включены между маркерами «#begin python» и «#end python», как показано ниже.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Расширение макроса PYM

Расширение макроса PYM представлено двумя последовательностями, т.е. <[ и ]>. Это специальные html-теги, которые могут появляться в любом месте строки. Небольшой пример PYM выглядит следующим образом.

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

Результат выполнения этого через PYM следующий:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Использованная литература ##

* [PYM — препроцессор макросов на основе Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Интерпретаторы PYM](https://github.com/interpreters/pym)

