{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PET - File Paket Instalasi Puppy Linux",
  "description":"Pelajari tentang format file PET dan API yang dapat membuat dan membuka file PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Apa itu file PET Linux?

File PET adalah file paket instalasi aplikasi yang dibuat dan digunakan dengan varian PuppyLinux dari Sistem Operasi Linux. Itu dibuat sebagai file [TGZ](/id/compression/tgz/) terkompresi yang mengurangi ukuran file dari arsip terkompresi. Integritas format file PET dipastikan dengan checksum md5sum yang ditambahkan ke akhir file untuk verifikasi di ujung jarak jauh. File PET dapat diekstraksi menggunakan ekstraktor file TGZ standar dan WinRAR. File PET menggantikan file instalasi paket [PUP](/id/compression/pup/) lama.

## Format File PET

File PET disimpan ke disk sebagai arsip terkompresi dalam format file biner. Namun, detail format file internal dari format file PET tidak diketahui. Mirip dengan file penginstalan paket [.exe](/id/executable/exe/) dan [.msi](/id/executable/msi/), file PET memulai penginstalan saat dijalankan.

## Referensi

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Indeks paket PET PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

