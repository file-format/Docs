{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "Paket Aplikasi Tingkat Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DACPAC dan API yang dapat membuat dan membuka file DACPAC.",
  "title" :"DACPAC - Paket Aplikasi Tingkat Data",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Apa itu file DACPAC?

File dengan ekstensi .dacpac (singkatan dari Data Tier AppliCation Package) adalah file database, dibuat dengan aplikasi data tier Microsoft SQL Server, yang berisi model database untuk representasi objek database. Karena berisi model database yang lengkap, ini digunakan untuk memulihkan database dari detail yang tersedia di model. File DACPAC biasanya diserahkan ke tim penerapan untuk dipasang di lokasi pelanggan guna memulihkan database. Ini bisa dibuka dengan
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Format File DACPAC - Informasi Lebih Lanjut

File paket data DACPAC sebenarnya adalah file ZIP terkompresi yang berisi beberapa file [XML](/id/web/xml/) yang berisi informasi tentang model database, seperti tabel dan tampilan, yang digunakan untuk memulihkan database. Untuk melihat konten file DACPAC, ganti nama file dari .dacpac menjadi [.zip](/id/compression/zip/) dan ekstrak arsip zip menggunakan utilitas dekompresi apa pun.

Berikut adalah beberapa file yang ditemukan di dalam file DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* model.xml

Perlu dicatat bahwa DACPAC tidak berisi DATA dan objek tingkat server lainnya. File tersebut dapat berisi semua jenis objek yang mungkin disimpan dalam proyek SSDT.

## Referensi

* [Aplikasi Tingkat Data - Manfaat](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Menerapkan Aplikasi Tingkat Data - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Bagaimana cara membuat File DACPAC?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

