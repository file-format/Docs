{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file ACCDT dan API yang dapat membuat dan membuka file ACCDT.",
  "title" :"ACCDT - Format File Basis Data Templat Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Apa itu file ACCDT?

File dengan ekstensi .accdt adalah file template database Microsoft Access yang berisi elemen database yang telah ditentukan sebelumnya. Elemen-elemen ini adalah kumpulan struktur yang mendefinisikan aplikasi basis data seperti skema basis data untuk menyimpan data, deskripsi tata letak untuk tampilan data, dan metadata yang menjelaskan basis data. Menjadi file template, file ACCDT dapat digunakan untuk membuat database berdasarkan pengaturan template yang tersedia di dalamnya. File database yang dihasilkan disimpan sebagai file [ACCDB](/id/database/accdb/) dan diisi dengan data dalam tabel. Microsoft Access 2007 dan seterusnya dapat membuka file ACCDT.

## Format File ACCDT

File template ACCDT didasarkan pada spesifikasi Office Open XML dan semua data terdapat dalam paket ZIP. Informasi struktur dan konten database terdapat dalam file [XML](/id/web/xml/) dan file teks dan ditautkan satu sama lain melalui hubungan. Anda dapat mengganti nama file ACCDT menjadi ekstensi [.zip](/id/compression/zip/) dan menggunakan perangkat lunak kompresi apa pun untuk mengekstrak konten arsip ZIP.

### Struktur file

File ACCDT adalah paket yang berisi kumpulan bagian terkait. Setiap **bagian** menyimpan informasi tentang konten aplikasi database menggunakan format XML, teks, dan biner, yang meliputi:

* Objek basis data
* Metadata terkait
* Struktur paket

#### Kemasan

Paket adalah arsip [ZIP](/id/compression/zip/) yang berisi beberapa bagian dan sesuai dengan Konvensi Kemasan Terbuka yang ditentukan dalam [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). File ACCDT harus berisi minimal satu bagian metadaa Templat yang harus menjadi target hubungan. Template Metadata ini adalah bagian awal dari file ACCDT.

#### Bagian

Bagian adalah aliran byte yang memiliki tipe terkait untuk menentukan sifat dan tipe konten yang disimpan di dalamnya. Pencacahan bagian menentukan bagian yang valid, tipe konten yang valid, dan hubungan yang diperlukan antara semua bagian dalam sebuah paket.

#### Hubungan

`Paket Hubungan` - di mana target adalah bagian dan sumber adalah paket secara keseluruhan.

`Part-to-Part Relationship` - di mana target adalah bagian dan sumber adalah bagian dalam paket.

`Hubungan Eksplisit` - di mana sumber daya direferensikan dari konten bagian sumber dengan mereferensikan elemen hubungan dengan nilai atribut ID-nya.

`Hubungan Implisit` - hubungan yang tidak eksplisit.

`Hubungan internal` - di mana target adalah bagian dari paket.

`Hubungan eksternal` - di mana targetnya adalah sumber daya eksternal yang tidak ada dalam paket.

## Referensi ##

* [Mengakses Format File Templat](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

