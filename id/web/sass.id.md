---
date: 2019-10-11
keywords: sass, .sass, format file sass, cara membuka file sass, stylesheet yang mengagumkan secara sintaksis, preprosesor css, sass
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File SAS
linktitle: Sass
description: "Pelajari tentang format file Sass dan API yang dapat membuat dan membuka file Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Apa itu file SASS? ##

Sass (style sheet yang mengagumkan secara sintaksis) adalah bahasa skrip preprosesor. Ini dikompilasi ke dalam [CSS](/id/web/css/) dan disimpan dengan ekstensi .sass. Sass terdiri dari dua sintaks, yang asli berdasarkan lekukan yang menggunakan ekstensi .sass dan SCSS yang lebih baru dengan pemformatan blok seperti CSS yang menggunakan ekstensi .scss.

## Mengapa menggunakan Sass ##

Sass sangat membantu dalam mempertahankan gaya karena menyediakan banyak fitur seperti memperkenalkan variabel, bersarang, mixin, impor, dan pewarisan pemilih yang membuat bekerja dengan gaya menjadi menyenangkan.

## Cara menggunakan file SASS ##

File SASS tidak disertakan secara langsung dalam dokumen [HTML](/id/web/html/) melainkan dikonversi ke file CSS yang disertakan dalam file HTML. Anda dapat menginstal Sass sistem Anda dengan mengikuti petunjuk yang diberikan di [Situs Resmi Sass](https://sass-lang.com/install).

Sass dapat dikonversi ke CSS dengan mengonversi file SASS yang sudah disimpan atau dengan mengamati perubahan dan mengonversi saat file disimpan. Perintah untuk keduanya diberikan di bawah ini.

### Mengkonversi Sekali ###

Parameter pertama dari perintah adalah file sumber SASS dan parameter kedua adalah file output CSS.

```cmd
sass main.sass main.css
```

### Perhatikan Perubahan ###

Perintah di atas dapat dijalankan dengan flag *watch* tambahan yang membuat perintah tetap berjalan dan segera setelah file Sass disimpan, keluaran CSS dihasilkan.

```cmd
sass --watch main.sass main.css
```

## Sintaks Sass ##

Sass mendukung variabel, nesting, mixin, impor, pewarisan pemilih, dll. Diberikan di bawah ini adalah contoh dari fitur-fitur ini.

### Variabel ###

Variabel dapat digunakan untuk mengatur informasi yang dapat digunakan kembali seperti warna primer atau padding untuk tombol. Ini terbukti berguna jika di masa mendatang Anda perlu mengubah informasi itu, Anda cukup mengubahnya di satu lokasi dan diperbarui di mana-mana.

**Kelancangan**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS yang dihasilkan**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Bersarang ###

Pemilih CSS dapat bersarang mirip dengan hierarki HTML. Dalam contoh berikut, span bersarang di dalam blok h1.

**Kelancangan**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS yang dihasilkan**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Campuran ###

Mixin digunakan untuk mengelompokkan properti serupa bersama-sama yang digunakan di banyak tempat. Mixin juga mendukung parameter.

**Kelancangan**

**Mendeklarasikan mixin**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Menggunakan mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**CSS yang dihasilkan**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Memperpanjang ###

Perpanjang/Pewarisan dapat terbukti bermanfaat dalam kasus di mana properti dari satu pemilih perlu dibagikan dengan pemilih lainnya. Pada contoh di bawah, pemilih *.error-notice* mengambil semua properti dari pemilih *.error-text* dan menambahkan properti border dan padding.

**Kelancangan**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**CSS yang dihasilkan**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Impor ###

Mengimpor dapat berguna jika Anda menyusun gaya Anda ke dalam file yang berbeda berdasarkan fungsionalitas atau struktur lain yang Anda ikuti. Anda dapat mengimpor semua file ini dalam file SASS utama yang kemudian diubah menjadi CSS. Saat mengimpor, Anda tidak perlu menentukan ekstensi file dalam instruksi impor. Sass mengkompilasi semua file SASS secara langsung. Untuk menghindari mengimpor file untuk dikompilasi secara langsung, Anda dapat membuatnya sebagian dengan menambahkan garis bawah (_) di awal namanya. Partial diimpor mirip dengan file Sass normal.

**Kelancangan**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Output CSS akan memiliki gaya dari semua file yang diimpor.

## Referensi ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

