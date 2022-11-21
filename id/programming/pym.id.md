---
date: 2022-05-09
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format File PYM - File Praprosesor Makro PYM
linktitle: PYM
description: "Pelajari tentang format file PYM dan API yang dapat membuat dan membuka file PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Apa itu file PYM?

File PYM adalah file preprocessor makro berdasarkan bahasa pemrograman Python. Ini dikembangkan oleh VRVis Research dan menyimpan pintasan makro. Saat file PYM diinterpretasikan oleh tahap preprocessing juru bahasa Python, pintasan ini diperluas sebagai pengganti teks lengkapnya. Selain itu, operasi opsional ketiga yang dapat dilakukan oleh preprosesor makro adalah penyertaan file. File PYM dapat dibuka di editor teks seperti Notepad, Notepad++, Apple TextEdit, dan VI di Linux.

## Format File PYM

File PYM disimpan sebagai file teks biasa ke disk. File PYM juga dapat menyertakan file lain menggunakan direktif `#include`.

### Sintaks PYM

Pernyataan PYM disertakan di antara penanda ""#begin python dan "#end python" seperti yang ditunjukkan di bawah ini.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Ekspansi Makro PYM

Ekspansi makro PYM diwakili oleh dua urutan yaitu <[ dan ]>. Ini adalah tag html khusus dan dapat muncul di mana saja dalam satu baris. Sedikit contoh PYM adalah sebagai berikut.

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

Output menjalankan ini melalui PYM adalah sebagai berikut:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referensi ##

* [PYM - Preprosesor Makro Berdasarkan Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Penerjemah PYM](https://github.com/interpreters/pym)

