---
date: 2019-10-11
keywords: js, .js, format file js, cara membuka file js, file javascript
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Berformat JS
linktitle: JS
description: "Pelajari tentang format file JS dan API yang dapat membuat dan membuka file JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Apa itu file JS? ##

JS (JavaScript) adalah file yang berisi kode JavaScript untuk dieksekusi di halaman web. File JavaScript disimpan dengan ekstensi .js. Di dalam dokumen [HTML](/id/web/html/), Anda dapat menyematkan kode JavaScript menggunakan \ <script>\</script> tag atau sertakan file JS. Mirip dengan file [CSS](/id/web/css/), file JS dapat disertakan dalam beberapa dokumen HTML untuk penggunaan ulang kode. JavaScript dapat digunakan untuk memanipulasi DOM HTML.

## Sejarah Singkat ##

JavaScript pertama kali dikirimkan sebagai bagian dari Browser Navigator pada bulan September 1995 dengan nama LiveScript oleh Netscape. Itu berganti nama menjadi JavaScript tiga bulan kemudian. Pada tahun 1996, Microsoft merekayasa ulang juru bahasa Navigator untuk membuat JScript. JScript dirilis dengan Internet Explorer dan sangat berbeda dari JavaScript.

Netscape mengirimkan JavaScript ke ECMA International yang mengarah pada rilis resmi spesifikasi ECMAScript pertama pada tahun 1997. ECMAScript 2 dirilis pada tahun 1998, ECMAScript 3 pada tahun 1999, dan pengerjaan ECMAScript 4 dimulai pada tahun 2000 tetapi tidak pernah membuahkan hasil.

Jesse James Garrett pada tahun 2005 merilis kertas putih di mana dia menciptakan istilah *Ajax*. Ini menggunakan JavaScript sebagai tulang punggung untuk membuat aplikasi web yang memuat data di latar belakang dan menghindari pemuatan ulang halaman penuh. Ini menghasilkan pembuatan perpustakaan seperti JQuery, Prototype, Dojo, dll.

Google merilis browser Chrome dengan mesin JavaScript V8 pada tahun 2008. Pada awal tahun 2009, sebuah perjanjian dibuat untuk menggabungkan semua pekerjaan yang relevan dan untuk memajukan JavaScript. Ini menghasilkan rilis Standar ECMAScript 5 pada bulan Desember 2009.

## Cara menggunakan file JS ##

Untuk menggunakan file JS, Anda memasukkannya ke dalam dokumen HTML. Anda menggunakan tag tautan untuk memasukkan file seperti yang ditunjukkan di bawah ini.

```html
<script src="site.js"></script>
```

Atribut *src* dari tag *script* berisi jalur ke file JS. Dengan melakukan ini, fungsionalitas JS ditambahkan ke dokumen HTML.

## Sintaks JS ##

File JavaScript dapat berisi variabel, operator, fungsi, kondisi, loop, array, objek, dll. Diberikan di bawah ini adalah gambaran singkat tentang sintaks JavaScript.

- Setiap perintah diakhiri dengan titik koma (;).
- Gunakan kata kunci *var* untuk mendeklarasikan variabel.
- Mendukung operator aritmatika ( + - * / ) untuk menghitung nilai.
- Komentar satu baris ditambahkan dengan // dan komentar multibaris diapit oleh /* dan */.
- Semua identifier bersifat case-sensitive yaitu *modelNo* dan *modelno* adalah dua variabel yang berbeda.
- Fungsi ditentukan dengan menggunakan kata kunci *fungsi*.
- Array dapat didefinisikan menggunakan tanda kurung siku [].
- JS mendukung operator pembanding seperti ==, != , >=, !==, dll.
- Kelas dapat didefinisikan menggunakan kata kunci *class*.

## Contoh Penggunaan JS ##

Berikut ini adalah contoh penggunaan file JavaScript sederhana.

### Dokumen HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Kode JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referensi ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

