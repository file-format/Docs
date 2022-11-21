{
  "date" : "2021-07-08",
  "keywords" :["HAR", "File", "Ekstensi", "Format File", "Ekstensi File", "JSON", "File Arsip"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Format File Arsip HTTP",
  "description" :"Panduan format file Anda untuk mempelajari apa itu file HAR dan API yang dapat membuat dan membuka file HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Apa itu file HAR?

File dengan file .har ([HTTP](/id/web/http/) Archive) adalah file arsip HTTP yang menyimpan transfer data sesi melalui banyak browser (seperti Chrome, Safari, IE, Firefox, dll.) di [JSON] (/id/web/json/) format file. Data yang ditransfer melalui internet antara server dan klien (dalam hal ini browser pengguna) berisi header permintaan dan respons HTTP yang disimpan dalam file HAR. Lebih lanjut berisi informasi terperinci tentang data kinerja tentang halaman web yang dimuat di browser. File HAR dapat dibuka di editor teks apa pun seperti Notepad di Microsoft Windows OS dan TextEdit di Apple MacOS.

## Format File HAR - Informasi Lebih Lanjut

File HAR menyimpan informasi sesi dalam file teks biasa menggunakan format JSON yang populer. Spesifikasi untuk format file HAR dibuat oleh Web Performance Group dari World Web Consortium (W3C) tetapi tidak dapat dipublikasikan. Namun, itu berhasil menentukan format arsip untuk transaksi HTTP.

Selain memantau transfer informasi permintaan dan respons, file HAR digunakan oleh pengembang untuk mencatat kinerja browser web dalam hal kecepatan pemuatan halaman, durasi pemuatan konten, pemuatan konten, kueri yang dijalankan untuk mendapatkan respons dari browser, dan banyak lainnya. .

## Mengapa menggunakan file HAR?

File HAR dapat membantu dalam meningkatkan kinerja situs web dengan mengevaluasi waktu muat yang lama, waktu rendering halaman, dan waktu respons. File HAR dapat dianalisis untuk menemukan masalah seperti itu dan menyelesaikan masalah apa pun dengan situs web untuk meningkatkan kinerja.

## Bagaimana cara menghasilkan file HAR?

Jadi, bagaimana cara menghasilkan file HAR? Ini tergantung pada jenis browser yang Anda gunakan untuk menghasilkan file HAR. Dalam panduan ini, kami mencantumkan langkah-langkah untuk browser Google Chrome. Metode untuk menghasilkan file HAR menggunakan Safari, Firefox, dll dapat dengan mudah dicari di internet dan diikuti.

### Langkah-langkah untuk Menghasilkan file HAR menggunakan Google Chrome

Langkah-langkah berikut dapat dilakukan pada halaman web di mana masalah sedang dihadapi.

1. Buka halaman web di Google chrome tempat masalah terjadi.
1. Buka alat pengembang (periksa elemen).
1. Pergi ke kiri panel untuk memulai perekaman file. Ada tombol merah bulat kecil di bagian ini.
1. Klik untuk "Hapus ikon" untuk menghapus semua catatan log yang disimpan di browser.
1. Untuk menyimpan konten yang diinginkan seperti gambar di atas, klik kanan dan klik “Save as HAR File”

## Referensi

* [Format File HAR - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

