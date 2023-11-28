{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADM - Format File Templat Administratif",
  "description":"Pelajari tentang format file ADM dan cara membuka file ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Apa itu file ADM?

File ADM adalah file templat yang digunakan oleh perangkat lunak Kebijakan Grup Microsoft untuk menentukan lokasi pengaturan kebijakan berbasis registri di file registri. Ini digunakan oleh administrator sistem untuk menentukan kebijakan pengelolaan sekelompok komputer yang merupakan bagian dari grup. Informasi ini menjadi bagian dari Objek Kebijakan Grup (GPO) yang dibuat untuk pengelolaan grup.

Anda dapat membuka file ADM menggunakan Editor Objek Kebijakan Grup Microsoft.

## Format File ADM - Informasi Lebih Lanjut

File ADM disimpan sebagai file teks berformat unicode. Ini terutama digunakan untuk mengetahui lokasi pengaturan kebijakan berbasis registri di registri Windows Vista dan Windows 7.

File ADM tidak lagi didukung dan telah digantikan oleh file [ADMX](/id/system/admx/). GPA mengabaikan file ADM default berikut pada komputer yang menjalankan Microsoft Windows Vista Service Pack 1 atau lebih baru.

* sistem.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Referensi

* [File Templat Administratif - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Mengelola File Templat Administratif](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

