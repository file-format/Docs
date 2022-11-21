{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Ekstensi File INC - Apa itu file INC?",
  "description":"Pelajari tentang INC Sertakan format file dan API yang dapat membuat dan membuka file INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Apa itu file INC?

File INC adalah file penyertaan yang digunakan oleh kode sumber program perangkat lunak untuk mereferensikan informasi header. Mirip dengan [format file .h](/id/programming/h/) dan berisi deklarasi, fungsi, header, atau makro yang dapat digunakan kembali oleh file kode sumber seperti C++. File INC digunakan oleh berbagai bahasa pemrograman seperti C, [C++](/id/programming/cpp/), Pascal, [PHP](/id/programming/php/), dan [Java](/id/programming/java/). Editor teks seperti Microsoft Notepad, Notepad++, dan TextEdit dapat digunakan untuk membuka file INC.

## Format File INC - Informasi Lebih Lanjut

File INC disimpan sebagai file teks biasa dengan semua deklarasi disertakan sesuai sintaks deklarasi. Satu file INC juga dapat mereferensikan file INC lainnya. Setelah dibuat, file INC menjadi bagian dari proyek dan dapat dirujuk dari file sumber seperti C++. Itu dapat dirujuk oleh banyak file sumber untuk menghindari duplikasi apa pun.

## Isi File INC

File INC dapat menyertakan informasi berikut.

**`Variabel`** - Dalam kasus Pemrograman Berorientasi Objek (OOP), file header kelas berisi definisi semua variabel tingkat kelas yang dapat diakses di seluruh file kode sumber implementasi

**`Deklarasi Metode`** - Semua deklarasi metode disertakan dalam file header .h agar dapat diakses di beberapa file implementasi.

**`Non-Inline Function Definitions`** - File header juga dapat berisi definisi metode non-inline.

## Kerugian menggunakan file INC di PHP

PHP adalah skrip sisi server yang berjalan di server dan mengembalikan hasilnya ke halaman web pemanggil. Jika file PHP mereferensikan file INC dan server tidak dikonfigurasi untuk mengurai file .inc (yang sangat umum), pengguna dapat melihat kode sumber php di file .inc dengan mengunjungi direktori URL. Jadi, seseorang harus berhati-hati saat menggunakan file INC sebagai file yang disertakan dalam PHP.

## Referensi

* [Menggunakan INC di PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

