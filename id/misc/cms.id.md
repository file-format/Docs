{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File CMS - File Profil Layanan Connection Manager",
  "description":"Pelajari tentang file CMS dan API yang dapat membuat dan membuka file CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Apa itu file CMS?

File CMS adalah file data yang berisi informasi profil yang digunakan oleh Microsoft Windows Connection Manager. Ini memungkinkan pengguna jarak jauh terhubung ke jaringan menggunakan informasi profil ini. Informasi yang disimpan di dalam file CMS mencakup data tentang sistem operasi pengguna dan izin yang digunakan untuk membuat sambungan antara pengguna jarak jauh dan jaringan. Administrator CMS menggunakan Connection Manager Administrator Kit (CMAK) untuk membuat file CMS.

## Format File CMS - Informasi Lebih Lanjut

File CMS tidak ditemukan secara umum di mesin pengguna. Karena ini digunakan secara khusus untuk memungkinkan pengguna jarak jauh ke jaringan, Anda akan menemukan ini di komputer yang digunakan untuk menyambung ke jaringan perusahaan atau beberapa kantor khusus yang dibangun untuk tujuan tertentu. Dalam kebanyakan kasus, itu digunakan untuk terhubung ke jaringan organisasi seperti Virtual Private Network (VPN) yang didedikasikan hanya untuk perusahaan. Menjadi administrator jaringan, Anda akan mengatur akses ke jaringan tersebut dengan Connection Manager untuk mengizinkannya mengakses jaringan perusahaan dari lokasi jarak jauh.

### Apa itu CMS insdie?

File profil CMS dibuat menggunakan Connection Manager dan dikemas dengan file konfigurasi lain sebelum diberikan kepada pengguna jarak jauh. File tambahan ini mungkin menyertakan file CMP dan dan file INF yang dikemas bersama dalam file [EXE](/id/executable/exe/). Paket lengkap ini disediakan untuk pengguna jarak jauh untuk terhubung ke jaringan.

## Referensi

* [Memahami dan mengonfigurasi Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

