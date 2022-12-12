---
date: 2022-05-09
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM файлов формат - PYM Macro Preprocessor File
linktitle: PYM
description: "Научете за PYM файловия формат и API, които могат да създават и отварят PYM файлове."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Какво е PYM файл?

PYM файлът е макропрецесорен файл, базиран на езика за програмиране Python. Разработен е от VRVis Research и съхранява преки пътища за макроси. Когато PYM файлът се интерпретира от етапа на предварителна обработка на интерпретатора на Python, тези преки пътища се разширяват като заместители на пълния им текст. В допълнение, трета незадължителна операция, която може да бъде извършена от препроцесор на макроси, е включването на файл. PYM файловете могат да се отварят в текстови редактори като Notepad, Notepad++, Apple TextEdit и VI на Linux.

## PYM файлов формат

PYM файловете се записват като обикновени текстови файлове на диск. PYM файл може също да включва други файлове, използвайки директивата `#include`.

### Синтаксис на PYM

Изявленията на PYM са включени между маркерите "" #begin python и "#end python", както е показано по-долу.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Макро разширяване

Разширяването на PYM макроса е представено от две последователности, т.е. <[ и ]>. Това са специални html тагове и могат да се появят навсякъде в ред. Малък пример за PYM е както следва.

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

Резултатът от изпълнението на това през PYM е както следва:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Препратки ##

* [PYM - Макро препроцесор, базиран на Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Интерпретатори на PYM](https://github.com/interpreters/pym)

