{
  "date" : "2021-08-10",
  "keywords" :[ "file .ovf", "format file", "apa itu file .ovf", "file", "ekstensi file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang apa itu format file .ovf dan API yang dapat membuat dan membuka file OVF.",
  "title" :"Format File OVF - Buka File Virtualisasi",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Apa itu file OVF?

File OVF adalah file teks yang berisi informasi tentang pengemasan dan distribusi perangkat lunak yang berjalan di mesin virtual. Ini diformat sesuai [Spesifikasi Standar Virtualisasi Terbuka](https://www.dmtf.org/standards/ovf) yang menjelaskan semua persyaratan (seperti keamanan, portabilitas, efisiensi, dan ekstensibilitas) untuk menjalankan aplikasi di mesin virtual. Organisasi Internasional untuk Standardisasi (ISO) telah mengadopsi OVF sebagai standar ISO 17203.

## Sejarah Singkat Format File OVF

Format file OVF diperkenalkan oleh DMTF (Satuan Tugas Manajemen Terdistribusi) yang menciptakan standar pengelolaan terbuka. Itu tidak tergantung pada hypervisor atau arsitektur set instruksi tertentu. Paket OVF berisi satu atau lebih sistem virtual, yang masing-masing dapat digunakan ke mesin virtual.

## Format File OVF - Informasi Lebih Lanjut

Paket OVF terdiri dari banyak file yang ditempatkan dalam satu direktori. Di antaranya, terdapat tepat satu file deskriptor OVF (dengan ekstensi .ovf) yang disimpan dalam format file [XML](/id/web/xml/). Ini menjelaskan informasi mesin virtual terpaket dan informasi metadata tentang paket OVF seperti:

* nama
*persyaratan perangkat keras
* referensi ke file lain dalam paket OVF, dan
* deskripsi yang dapat dibaca manusia

File lain yang dapat ditemukan dalam paket OVF termasuk satu atau lebih gambar disk dan file sertifikat opsional dan file tambahan lainnya.

## Referensi

* [Format Virtualisasi Terbuka - DMTF](https://www.dmtf.org/standards/ovf)
* [Spesifikasi Format File OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

