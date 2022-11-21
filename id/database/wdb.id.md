{
  "date" : "2021-08-24",
  "keywords" :[ "file wdb", "format file wdb", "apa itu file wdb", "file", "contoh wdb", "ekstensi file wdb", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file WDB dan API yang dapat membuat dan membuka file WDB.",
  "title" :"WDB - File Pelacakan SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Apa itu file WDB?
File dengan ekstensi .wdb sebenarnya adalah file database yang dibuat oleh Microsoft Works yang digunakan untuk menjalankan fungsi seperti sistem manajemen database. File WDB serupa dengan file Access Database ([MDB](/id/database/mdb/)), tetapi kurang efisien dan memiliki batasan yang lebih besar. File WDB tidak dapat dibuka dengan menggunakan Microsoft Access. Namun, Anda dapat membuka file WDB di Microsoft Works dan kemudian mengekspornya ke file MDB, untuk membuka file WDB di MS Access.

## format file WDB
Basis Data Microsoft Works adalah format basis data asli dari suite kantor Microsoft Works. Karena sifat kepemilikan format dan beberapa keterbatasan. File WDB tidak dapat dibuka di perangkat lunak lain selain Microsoft Works. Dalam format file berulang, header 10 byte dapat ditemukan sebelum masing-masing string teks ASCII yang mewakili nilai bidang yang diakhiri dengan nilai NULL. Header umumnya dimulai dengan byte **\x0f** dan NULL, diikuti oleh 4 byte data yang diselingi dengan NULL.

### Struktur file

Struktur file WDB diberikan di bawah ini:
- **1st header**: dari awal file, diakhiri dengan \x25\x00\xf2 dan 244 NULL byte
- **header ke-2**: dimulai dengan \xffT - yaitu \xff\x54 dan diperluas hingga 4096 byte, yang berisi nama kolom/bidang dan hal lainnya, dan sepertinya dimulai pada posisi byte 6144.
- **Field**: nilai memiliki header 10 byte, dengan format berikut: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , bagian 2} {db 4} \x00. byte data 2 adalah nomor bidang, byte data 3 adalah nomor record (menambahkan byte data 3, bagian 2 saat melebihi 256 record).


## Referensi ##

* [Pengguna:JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

