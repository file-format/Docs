{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADMX - Format File Templat Administratif Kebijakan Grup",
  "description":"Pelajari tentang format file ADMX dan cara membuka file ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Apa itu file ADMX?

File ADMX adalah file konfigurasi kebijakan yang digunakan oleh perangkat lunak Kebijakan Grup Microsoft Windows yang mengelola sekelompok komputer dalam satu grup. Ini adalah file templat administratif berbasis XML dan diperkenalkan dengan Windows Vista Service Pack 1. File ADMX berisi pengaturan konfigurasi untuk akun pengguna, konfigurasi sistem operasi, dan aplikasi. File ADMX digunakan untuk menyimpan dan menyebarkan konfigurasi untuk manajemen terpusat di banyak sistem komputer.

Anda dapat membuat atau mengedit file ADMX menggunakan editor teks apa pun yang kompatibel dengan XML, atau Editor Objek Kebijakan Grup Microsoft.

## Format File ADMX - Informasi Lebih Lanjut

File ADMX disimpan dalam format file universal [XML](/id/web/xml/) yang dapat dibaca manusia. Ini adalah format file multibahasa dan memungkinkan administrator sistem dari berbagai bahasa untuk bekerja dengan file ADMX yang sama. File ADMX menggantikan format file [ADM](/id/system/adm/) lama yang merupakan format file teks berformat unicode. File ADMX menentukan kunci registri yang diubah ketika pengaturan Kebijakan Grup tertentu diubah.

### Apa yang dapat saya lakukan dengan berkas ADMX?

File ADMX menentukan tindakan apa yang diperbolehkan untuk komputer pengguna yang merupakan bagian dari grup. Kebijakan grup menerapkan aturan yang ditetapkan bersama dengan perangkat lunak Direktori Aktif. File ADMX dikelola dari penyimpanan pusat pada OS Windows yang merupakan lokasi pusat dalam domain.

File ADMX yang diterapkan di lingkungan kerja dapat memungkinkan administrator menerapkan kebijakan seperti:

* Kontrol penggunaan internet
* Mengunduh jenis file tertentu
* Penggunaan perangkat yang dapat dilepas pada sistem

## Referensi

* [File Templat Administratif - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Mengelola File Templat Administratif](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

