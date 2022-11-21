{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File APPCACHE - Format File Manifes Cache HTML5",
  "description" :"Pelajari tentang apa itu file APPCACHE dan API yang dapat membuat dan membuka file APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Apa itu file APPCACHE?

File APPCACHE adalah file teks yang berisi daftar sumber daya yang akan di-cache oleh browser untuk akses offline ke aplikasi web. Ini berguna ketika tidak ada koneksi internet. Dalam situasi seperti itu, browser menggunakan sumber daya cache offline untuk menyediakan akses ke konten web. File APPCACHE berisi sumber daya web seperti gambar (misalnya **[PNG](/id/image/png/)**, **[WEBP](/id/image/webp/)**, dll.), stylesheet **([ CSS])(/id/web/css/)**, dan file skrip (seperti file Javascript **[JS](/id/web/js/)**).

Aplikasi yang dapat **membuka file APPCACHE** termasuk browser web seperti Google Chrome, Safari, dan Firefox.

## Format File APPCACHE - Informasi Lebih Lanjut

File APPCACHE adalah file teks sederhana, menyediakan akses offline ke halaman web untuk dijalankan tanpa koneksi internet. Kehadiran APPCACHE menunjukkan halaman sebagai tersedia offline.

### Bagaimana Referensi file APPCACHE?

Di halaman HTML Anda, file APPCACHE direferensikan sebagai berikut.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktur file Manifest APPCACHE

File manifes APPCACHE sederhana terlihat sebagai berikut.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Ini adalah contoh paling sederhana dan mungkin ada struktur yang lebih kompleks juga.

## Keuntungan Manifes APPCACHE

Penggunaan antarmuka cache memberi aplikasi web keuntungan sebagai berikut.

1. Penjelajahan Offline - Antarmuka cache memberikan pengguna akhir untuk menelusuri situs lengkap Anda saat mereka sedang Offline
1. Kecepatan - cache memungkinkan akses berkecepatan tinggi ke konten offline langsung dari disk
1. Aksesibilitas sepanjang waktu - Jika situs Anda down, pengguna masih memiliki akses ke konten web dan akan bisa mendapatkan pengalaman offline

## Referensi

* [Panduan Pemula untuk Manifes AppCache](https://web.dev/appcache-beginner/)

