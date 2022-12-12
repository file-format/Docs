---
date: 2022-05-09
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Формат файлу PYM – файл препроцесора макросів PYM
linktitle: PYM
description: "Дізнайтеся про формат файлів PYM та API, які можуть створювати та відкривати файли PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Що таке файл PYM?

Файл PYM — це файл препроцесора макросів на основі мови програмування Python. Він був розроблений VRVis Research і зберігає ярлики макросів. Коли файл PYM інтерпретується на етапі попередньої обробки інтерпретатора Python, ці ярлики розгортаються як заміна повного тексту. Крім того, третя, необов’язкова операція, яку може виконувати препроцесор макросу, — це включення файлу. Файли PYM можна відкривати в текстових редакторах, таких як Notepad, Notepad++, Apple TextEdit і VI в Linux.

## Формат файлу PYM

Файли PYM зберігаються на диск як звичайні текстові файли. Файл PYM також може містити інші файли за допомогою директиви `#include`.

### Синтаксис PYM

Оператори PYM включені між маркерами ""#begin python і "#end python", як показано нижче.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Розширення макросу PYM

Розгортання макросу PYM представлено двома послідовностями, тобто <[ і ]>. Це спеціальні теги html, які можуть з’являтися в будь-якому місці рядка. Невеликий приклад PYM виглядає наступним чином.

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

Результат виконання цього через PYM такий:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Посилання ##

* [PYM – препроцесор макросів на основі Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Інтерпретатори PYM](https://github.com/interpreters/pym)

