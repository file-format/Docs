{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Database Sqlite dari Proyek QGIS", "ekstensi", "format", "QGIS", "Database Tambahan", "Apa itu file QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Database Sqlite dari Proyek QGIS",
  "description":"Pelajari tentang QGD yang merupakan database sqlite dari proyek QGIS dan API yang dapat membuat dan membuka file QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Apa itu file QGD?

File dengan ekstensi file .QGD sebenarnya adalah database sqlite terkait dari proyek **QGIS** yang menampung data tambahan untuk proyek tersebut. File QGD akan tetap kosong jika tidak ada data tambahan untuk proyek tersebut.

## Detail tentang Format File QGD

Dalam mode klasik, database tambahan disimpan sebagai file dengan ekstensi .qgd di sepanjang file xml. Sistem **Auxiliary Database** memungkinkan untuk membaca dan menulis data dalam sistem sebagai cara alternatif. Saat Membuat QGZ yang merupakan wadah zip, file .qgd dimasukkan ke dalam .qgz.

## Apa itu Database Tambahan?
Auxiliary Database sebenarnya adalah sistem standby db yang dibuat sebagai respon dari duplikasi database target. Basis data tambahan sebenarnya adalah kasus basis data duplikat yang akan menjadi basis data tempat Anda menduplikasi. Misalnya jika Anda menyiapkan database siaga menggunakan database duplikat, database sumber akan menjadi target dan database siaga akan dikenal sebagai tambahan.


## Referensi

* [QGZ – Format file proyek default baru untuk QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Format File QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

