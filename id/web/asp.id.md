{
  "date" : "2019-10-11",
  "keywords" :[ "asp", "file asp", "format file asp", "tipe file asp", "file", "type", "apa itu file asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Format File Halaman Server Aktif",
  "description" :"Pelajari tentang apa itu file ASP dan API yang dapat membuat dan membukanya.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ASP?

ASP adalah singkatan dari Active Server Pages yang merupakan framework pengembangan untuk membuat halaman web. Ini memungkinkan kode komputer dijalankan oleh server internal untuk melayani permintaan web. Saat permintaan dibuat untuk file ASP oleh browser web, server membaca file tersebut dan mengeksekusi kode/skrip apa pun di dalamnya untuk menghasilkan hasil **[HTML](/id/web/html/)** yang dikembalikan ke browser untuk ditampilkan.

Tidak seperti halaman HTML, yang merupakan halaman statis yang dilayani oleh server, file ASP menghasilkan konten dinamis saat runtime yang mungkin melibatkan permintaan data dari database. Halaman ASP biasanya menggunakan ekstensi .asp daripada .html. Karena kode/skrip di dalam file ASP dijalankan di sisi server, browser yang meminta tidak dapat melihat kode yang digunakan untuk membuat halaman yang disajikan. Semua browser modern mampu menampilkan halaman yang dihasilkan sebagai hasilnya. Dibuat dengan teknologi Microsoft, halaman yang dibuat dengan ASP dihosting di server Layanan Informasi Internet (IIS) Microsoft.

## Sejarah Singkat Format File ASP
ASP telah melalui beberapa revisi hanya util itu digantikan oleh ASP.NET yang merupakan cara yang lebih modern dan lebih efisien untuk mengembangkan dan mengelola halaman sisi server. Dukungan untuk ASP disertakan secara default bersama dengan Layanan Informasi Internet (IIS). ASP diterbitkan dalam tiga versi berbeda dengan perbaikan di masing-masing versi.

* ASP 1.0 dirilis pada Desember 1996 sebagai bagian dari IIS 3.0
* ASP 2.0 dirilis pada September 1997 sebagai bagian dari IIS 4.0
* ASP 3.0 dirilis pada November 2000 sebagai bagian dari IIS 5.0

## Objek Fungsional ASP

File ASP menggunakan objek sisi server untuk memproses permintaan pengguna dan menghasilkan halaman keluaran untuk disajikan kepada pengguna. Setiap objek memiliki sekumpulan koleksi, properti, dan metode untuk memproses permintaan dan respons. Objek-objek tersebut meliputi:

### Objek Permintaan

Ketika browser meminta halaman dari server, itu disebut permintaan. Objek Permintaan digunakan untuk mendapatkan informasi dari pengunjung.

### Objek Respons

Objek ASP Response digunakan untuk mengirim output ke pengguna dari server.

### Objek Server

Objek ASP Server digunakan untuk mengakses properti dan metode di server. Ini memungkinkan koneksi ke database (ADO), sistem file, dan penggunaan komponen yang diinstal di server.

### Objek Sesi

Objek sesi seperti tautan antara browser pengguna yang meminta halaman dari server dan server itu sendiri. Ini dicapai dengan cookie yang dibuat oleh ASP dan dikirim ke komputer pengguna. Objek Sesi menyimpan informasi tentang, atau mengubah pengaturan untuk sesi pengguna. Informasi disimpan dalam objek Sesi yang dibagikan di semua halaman aplikasi. Informasi umum yang disimpan dalam variabel sesi adalah nama, id, dan preferensi. Server membuat objek Sesi baru untuk setiap pengguna baru, dan memusnahkan objek Sesi saat sesi berakhir.

### Objek Aplikasi

Objek Aplikasi menyimpan informasi yang akan digunakan oleh banyak halaman dalam aplikasi (seperti informasi koneksi database). Informasi dapat diakses dari halaman manapun. Informasi juga dapat diubah di satu tempat, dan perubahan tersebut akan secara otomatis tercermin di semua halaman. Objek Aplikasi digunakan untuk menyimpan dan mengakses variabel dari halaman manapun, seperti halnya objek Sesi.

### Objek ASPError

Objek ASPError diimplementasikan di ASP 3.0 dan tersedia di IIS5 dan yang lebih baruObjek ASPError digunakan untuk menampilkan informasi terperinci dari setiap kesalahan yang terjadi pada skrip di halaman ASP.

**Catatan:** Objek ASPError dibuat saat Server.GetLastError dipanggil, sehingga informasi kesalahan hanya dapat diakses dengan menggunakan metode Server.GetLastError.

## Referensi

* [ASP - Oleh W3C](https://www.w3schools.com/asp/default.asp)
* [Membuat Halaman ASP Sederhana](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

