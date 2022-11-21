---
date: 2021-07-05
keywords: ssp, .ssp, format file ssp, cara membuka file ssp, Scala Server Page
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Format File Halaman Server Scala
linktitle: SSP
description: "Pelajari tentang format file SSP dan API yang dapat membuat dan membuka file SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Apa itu file SSP?

File dengan ekstensi .ssp adalah halaman web yang dibuat dengan kode Scala untuk ekspresi, bukan hanya HTML biasa. Ini bertindak sebagai skrip sisi server menggunakan kombinasi HTML dan Scala. File-file ini berada di server dan digunakan untuk membuat halaman web statis untuk disajikan kepada pengguna. Scala sendiri adalah bahasa pemrograman serba guna yang sintaksisnya akrab bagi pengguna yang pernah bekerja dengan Velocity, JSP, atau Erb. File SSP dapat dianalisis dan dievaluasi menggunakan [Scalate](https://scalate.github.io/scalate/) yang merupakan mesin template berbasis Scala untuk membuat teks dan markup.

## Format File SSP - Informasi Lebih Lanjut

File SSP disimpan dalam file teks biasa dan dapat dievaluasi menggunakan Scalate. Template Ssp terdiri dari teks biasa yang lebih sering berupa dokumen HTML. Ini memiliki tag Ssp yang disematkan di dalamnya yang menyebabkan mesin rendering merender bagian dokumen yang berbeda secara dinamis. Tag dimulai dan diakhiri dengan urutan <% ... %> dan ${ ... } dan apa pun di luar ini dianggap sebagai teks literal.

### Contoh SSP

Contoh berikut menampilkan kode SSP dan outputnya saat dirender oleh mesin rendering.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Outputnya adalah sebagai berikut.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referensi

- [Referensi SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

