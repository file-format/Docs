---
date: 2019-10-11
keywords: css, .css, format file css, cara membuka file css, cascading style sheets
pengarang:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format File CSS
linktitle: CSS
description: "Pelajari tentang format file CSS dan API yang dapat membuat dan membuka file CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Apa itu file CSS? ##

CSS (Cascading Style Sheets) adalah file yang menjelaskan bagaimana elemen HTML ditampilkan di layar, kertas, dll. Dengan HTML, Anda dapat memiliki gaya tersemat atau gaya dapat ditentukan dalam lembar gaya eksternal. Untuk menyematkan gaya, \ <style>\</style> tag digunakan. Stylesheet eksternal disimpan dalam file dengan ekstensi .css. Dengan CSS eksternal, Anda dapat menyertakannya di beberapa halaman HTML untuk memperbarui gaya halaman tersebut. Bahkan satu file CSS dapat digunakan untuk mendesain situs web yang lengkap.

## Sejarah Singkat ##

CSS1 dirilis pada tahun 1996 dengan Bert Bos sebagai co-author. Kelompok Kerja CSS mulai menangani masalah yang tidak dibahas di CSS1. Ini menghasilkan pembuatan CSS2 pada November 1997 yang diterbitkan sebagai rekomendasi W3C pada 12 Mei 1998. Versi ini menambahkan dukungan untuk perangkat khusus media seperti printer, font yang dapat diunduh, tabel, dan pemosisian elemen. Pada Juni 1999, CSS3 menjadi rekomendasi W3C. Ini membagi dokumentasi menjadi modul di mana setiap modul memiliki fitur ekstensi yang ditentukan dalam CSS2.

## Cara menggunakan file CSS ##

Untuk menggunakan file CSS, Anda memasukkannya ke bagian kepala dokumen HTML. Anda menggunakan tag tautan untuk memasukkan file seperti yang ditunjukkan di bawah ini.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

atribut *href* dari tag tautan berisi jalur ke file CSS. Dengan melakukan ini, gaya yang berlaku yang terkandung dalam file CSS yang disertakan diterapkan ke dokumen HTML.

## Sintaks CSS ##

Aturan CSS terdiri dari dua komponen, pemilih dan deklarasi. Pemilih menunjuk ke elemen dalam dokumen HTML. Itu bisa berupa tag elemen, nama kelas, nama id, banyak tag yang menunjukkan hierarki, dll. Deklarasi berisi definisi gaya yang terdiri dari properti dan nilai. Properti mengidentifikasi properti elemen yang ingin Anda ubah dan nilainya menentukan nilai barunya. Setiap aturan CSS dapat memiliki beberapa deklarasi. Berikut ini adalah contoh aturan CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Pada contoh di atas, kita memiliki **h1** sebagai pemilih yang memilih semua tag h1 dalam dokumen HTML. Aturan memiliki dua deklarasi, satu untuk ukuran font dan yang lainnya untuk warna. *font-weight* dan *color* adalah properti dan *700* dan *forestgreen* adalah nilainya masing-masing.

## Contoh Penggunaan CSS ##

Berikut ini adalah contoh dokumen HTML dan stylesheet yang digunakan untuk menatanya. Gambar perbandingan juga ditambahkan untuk membandingkan dokumen HTML bergaya dan biasa

### Dokumen HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Lembar Gaya CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Perbandingan Keluaran ###

Sisi kiri gambar menampilkan dokumen HTML tanpa gaya yang diterapkan dan sisi kanan menampilkan dokumen HTML dengan gaya yang diterapkan.

{{< figure src="../CssExample.jpg" alt="Contoh gambar" >}}

## Referensi ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

