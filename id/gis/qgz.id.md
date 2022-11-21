{
  "date" : "2021-03-18",
  "keywords" :[ "file qgz", "format file qgz", "apa itu file qgz", "file", "contoh qgz", "ekstensi file qgz", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Proyek Terkompresi Quantum GIS",
  "description":"Pelajari tentang format file QGZ yang hanya berupa QGS dan API terkompresi yang dapat membuat dan membuka file QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Apa itu file QGZ?

Format file **QGZ** adalah arsip terkompresi yang berisi file [QGS](https://docs.fileformat.com/gis/qgs/) dan file QGD. Padahal, File QGD adalah database sqlite dari proyek qgis yang terdiri dari data tambahan untuk proyek tersebut. Jika tidak ada data tambahan, file QGD akan tetap kosong.

## Detail tentang Format File QGZ

QGZ diperkenalkan sebagai varian baru dari **format file proyek QGIS 3**. Format ini adalah wadah zip untuk file xml QGS. Jika pengguna memilih QGD yang merupakan format opsional, dalam hal ini wadah bermanfaat untuk menyimpan database penyimpanan tambahan.

Dalam mode klasik, database tambahan disimpan sebagai file dengan ekstensi .qgd di sepanjang file xml. Saat memilih wadah zip, file .qgd dimasukkan ke dalam .qgz, Ini hanya memfasilitasi pengguna tanpa masalah apa pun, pengguna tidak dapat menghapusnya atau lupa menyalinnya saat berbagi file proyek!


## Referensi

* [QGZ – Format file proyek default baru untuk QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Format File QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

