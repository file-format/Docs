{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg file", "apkg file format", "apkg file type", "file", "type", "Apa itu file APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Format File Dek Flashcard Anki",
  "description" :"Pelajari tentang apa itu file APKG dan API yang dapat membuat dan membukanya.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Apa itu file APKG?

File dengan ekstensi .apkg adalah setumpuk kartu flash yang dibuat untuk digunakan dalam aplikasi perangkat lunak [Anki](https://ankiweb.net/about) yang merupakan program pembelajaran berbasis kartu flash. Ini berisi teks [HTML](/id/web/html/) untuk dimuat dan ditampilkan dalam aplikasi Anki dan juga dapat memiliki gambar dan suara untuk pembelajaran visual dan suara. Anki memungkinkan pengguna untuk membuat deck kartu flash Anki mereka sendiri serta mengimpor deck kartu flash pengguna lain.

## Format File APK

Dek kartu Anki dibuat dari template yang ditulis dalam HTML, bahasa yang terkenal dan umum untuk membuat halaman web. Penataan gaya kartu dek dilakukan dengan menggunakan CSS yang merupakan bahasa yang digunakan untuk menata halaman web. Penataan mencakup modifikasi pada:

* font-family - Nama font yang akan digunakan pada kartu.
* font-size - Ukuran font dalam piksel.
* text-align - Menentukan apakah teks harus disejajarkan di tengah, kiri, atau kanan.
* warna - Menentukan warna teks yang dapat berupa nama warna sederhana seperti "biru", "merah", dll. atau kode warna HTML.
* background-color - Menentukan warna latar belakang kartu

Informasi gaya dibagikan di antara semua kartu, memengaruhi semua kartu saat perubahan dilakukan. Contoh berikut akan menggunakan latar belakang kuning pada semua kartu kecuali yang pertama:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Gambar yang diubah ukurannya dalam kartu Anki dapat dikontrol sebagai berikut.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Menyematkan Javascript di kartu Anki

Dimungkinkan untuk menyematkan [Javascript](/id/web/js/) di kartu Anki menggunakan templat kartu. Namun, karena Javascript tingkat lanjut, dukungannya tidak tersedia. Selain itu, perangkat rendering dapat menunjukkan pengaruh implementasi Javascript di kartu secara berbeda, sehingga diperlukan pengujian implementasi pada semua perangkat. Fitur Javascript tertentu seperti window.alert, membuat sulit untuk men-debug kode Javascript yang telah Anda tulis.

## Referensi ##

* [Dokumentasi Anki](https://docs.ankiweb.net/intro.html)

