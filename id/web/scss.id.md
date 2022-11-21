---
date: 2019-10-11
keywords: scss, .scss, format file scss, cara membuka file scss, stylesheet yang mengagumkan secara sintaksis, preprosesor css, sass
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File SCSS - Sass Cascading Style Sheet
linktitle: SCSS
description: "Pelajari tentang format file SCSS dan API yang dapat membuat dan membuka file SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Apa itu file SCSS? ##

SCSS adalah sintaks kedua dari Sass (Syntactically Awesome Stylesheet) yang menggunakan tanda kurung alih-alih lekukan. SCSS dirancang sedemikian rupa sehingga file CSS3 yang valid juga merupakan file SCSS yang valid. File SCSS disimpan dengan ekstensi .scss.

## Mengapa menggunakan SCSS ##

Karena desain situs web menjadi rumit sehingga menghasilkan file [CSS](/id/web/css/) yang besar. File seperti itu lebih sulit dipelihara. Di sinilah peran SCSS. SCSS memperkenalkan variabel, nesting, mixin, import, dan pewarisan pemilih dalam pengembangan CSS. Penambahan ini membuat bekerja dengan desain jauh lebih menyenangkan.

## Cara menggunakan file SCSS ##

File SCSS tidak disertakan langsung dalam dokumen [HTML](/id/web/html/) seperti CSS. Sebaliknya, file SCSS dikonversi ke file CSS yang disertakan dalam file HTML. Untuk menginstal SCSS di sistem Anda, ikuti petunjuk yang diberikan di [Situs Resmi Sass](https://sass-lang.com/install).
Untuk mengonversi SCSS ke CSS, Anda dapat mengonversi file SCSS yang sudah disimpan atau melihat perubahan dan mengonversi saat file disimpan. Perintah untuk keduanya diberikan di bawah ini.

### Mengkonversi Sekali ###

Parameter pertama adalah file SCSS sumber dan parameter kedua adalah file output CSS.

```cmd
sass main.scss main.css
```

### Perhatikan Perubahan ###

Perintah tersebut memiliki flag *watch** tambahan yang membuat perintah tetap berjalan dan segera setelah file SCSS disimpan, keluaran CSS dihasilkan.

```cmd
sass --watch main.scss main.css
```

## Sintaks SCSS ##

SCSS mendukung variabel, nesting, mixin, impor, pewarisan pemilih, dll. Diberikan di bawah ini adalah contoh dari fitur ini.

### Variabel ###

Dengan menggunakan variabel, Anda dapat mengatur informasi yang dapat digunakan kembali seperti warna primer atau warna latar belakang untuk tombol simpan. Ini berguna jika Anda perlu mengubah informasi itu, Anda cukup mengubahnya di satu lokasi dan memperbaruinya di mana pun digunakan.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Anda dapat menyarangkan pemilih CSS yang mirip dengan hierarki HTML. Dalam contoh yang diberikan di bawah ini, span bersarang di dalam blok h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Mixin dapat digunakan untuk mengelompokkan properti serupa yang digunakan bersama di banyak tempat. Anda juga dapat meneruskan parameter ke mixin.

**SCSS**

**Mendeklarasikan mixin**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Menggunakan mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Perluas/Pewarisan berguna dalam kasus di mana properti dari satu pemilih perlu dibagikan dengan pemilih lain. Pada contoh di bawah, pemilih *.error-notice* mengambil semua properti pemilih *.error-text* dan menambahkan properti border dan padding.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

Mengimpor dapat bermanfaat dalam pemisahan masalah. Anda dapat membagi gaya sedemikian rupa sehingga gaya tajuk berada dalam file terpisah, gaya footer berada dalam file terpisah, semua variabel warna yang digunakan dalam gaya dapat berada dalam file terpisah, dll. Dengan menggunakan teknik ini, gaya tetap teratur. Anda cukup mengimpor file di file SCSS utama Anda seperti yang ditunjukkan pada contoh di bawah ini. Anda tidak perlu menentukan ekstensi file dalam instruksi impor. Sass mengkompilasi semua file SCSS secara langsung. Untuk menghindari mengimpor file untuk dikompilasi secara langsung, Anda dapat membuatnya sebagian dengan menambahkan garis bawah (_) sebelum namanya. Anda dapat mengimpor sebagian yang mirip dengan file SCSS normal tanpa garis bawah.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Output CSS akan memiliki gaya dari semua file yang diimpor.

## Referensi ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

