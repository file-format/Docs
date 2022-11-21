{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HTACCESS - Format File Apache HTACCESS",
  "description" :"Panduan format file Anda untuk mempelajari apa itu file HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file HTACCESS?

File HTACCESS adalah file konfigurasi Apache yang menyediakan mekanisme untuk mengizinkan perubahan konfigurasi untuk berbagai folder/direktori situs web. Ini termasuk arahan konfigurasi yang berlaku untuk direktori dan sub-direktori.

File HTACCESS melakukan sejumlah pemeriksaan seperti menentukan halaman indeks situs web, mencantumkan halaman kesalahan 404 (Halaman Tidak Ditemukan), melakukan pengalihan halaman 301 atau 302, memblokir akses dari alamat IP tertentu atau situs web lain. Oleh karena itu, penggunaan file .htaccess memperlambat kinerja keseluruhan server [HTTP](/id/web/http/) Apache Anda.

## Format File HTACCESS

File HTACCESS disimpan ke disk dalam format file teks biasa. Ini berarti Anda dapat membuka dan mengedit file-file ini di editor teks apa pun. Tidak ada nama sebelum "." dalam file .htaccess, menunjukkan bahwa itu adalah file tersembunyi di dalam folder.

## Penggunaan umum File HTACCESS

Lima penggunaan umum file HTACCESS adalah sebagai berikut.

### Mod_Tulis ulang

File HTACCESS dapat digunakan untuk menentukan dan mengubah cara URL dan halaman web di situs web ditampilkan kepada pengguna.

### Autentikasi

Otentikasi dapat dicapai dengan .htaccess dengan membuat file passowrd bernama .htpasswd. Ini memungkinkan pengunjung situs untuk memberikan kata sandi jika mereka ingin mengunjungi bagian tertentu dari halaman web.

### Laman Kesalahan Khusus

Anda dapat membuat halaman kesalahan khusus seperti 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found dan 500 Internal Error dengan file .htaccess. Namun, ini akan memperlambat kinerja server karena semua pemeriksaan ini akan dijalankan saat halaman diakses.

### Jenis MIME

File Apache HTACCESS dapat dimodifikasi untuk menyertakan jenis Multipurpose Internet Mail Extensions (MIME). Ini memungkinkan server Anda mendukung pengiriman file aplikasi yang tidak didukung oleh situs.

###SSI

Termasuk Sisi Server (SSI) bertindak sebagai penghemat waktu yang hebat di situs web. SSI dapat diaktifkan dengan memasukkan kode hte berikut ke dalam file .htaccess Anda.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Contoh File Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referensi

* [Tutorial Server HTTP Apache: file .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

