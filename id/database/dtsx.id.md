{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "ekstensi", "file", "format file", "Jenis File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DTSX dan API yang dapat membuat dan membuka file DTSX.",
  "title" :"Format File DTSX - File Pengaturan SQL Server DTS",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Apa itu file DTSX?

File dengan ekstensi .dtsx (Data Transformation Services Package XML) adalah file Data Transformation Services (DTS) yang digunakan oleh Microsoft SQL untuk merujuk langkah/aturan migrasi data untuk transfer data dari satu database ke database lainnya. Ini termasuk transformasi dan setiap langkah pemrosesan opsional yang mungkin diperlukan selama transfer data antara titik asal dan tujuan. SQL Server Integration Services (SSIS), sebuah komponen dari Microsoft SQL Server, menggunakan file DTSX untuk mengidentifikasi langkah-langkah pemrosesan data antar server database. File DTSX dapat dibuka dengan Microsoft SQL Server 2019.

## Format File DTSX

Perpindahan data antar server basis data membutuhkan aturan dan langkah pemrosesan untuk memastikan integritas data selama operasi ini. SSIS memastikan bahwa semua aktivitas ini, untuk memindahkan dan menyesuaikan data dari berbagai sumber di perusahaan, berlangsung dengan nyaman. Di situlah DTSX datang yang menentukan struktur yang akan digunakan oleh SSIS untuk menetapkan langkah-langkah di mana data dapat diproses saat mengikuti langkah-langkah ini.

Aliran data yang dijelaskan oleh DTSX adalah seperti yang ditunjukkan pada gambar berikut.

{{< figure src="../DataFlowDTSX.png" alt="Aliran Data DTSX" >}}

DTSX berbasis [XML](/id/web/xml/) dan didokumentasikan dalam [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). Peningkatan pemfaktoran ulang DTSX XML adalah DTSX 2.0 yang menyertakan atribut baru ke struktur, penggantian properti bernama sebagai atribut XML induk, menentukan default untuk sebagian besar nilai atribut, dan penempatan elemen berulang di dalam elemen induk. Struktur DTSX dijelaskan menggunakan [Skema XML](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) dan format strukturalnya adalah XML teks celar.

## Referensi

* [Format DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Format DTSX 2 - Oleh Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

