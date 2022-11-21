{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File CPG - File Halaman Kode ESRI",
  "description":"Pelajari tentang format file CPG dan API yang dapat membuat dan membuka file CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Apa itu file CPG?

File CPG adalah file opsional yang memerlukan ESRI Shapefile yang digunakan untuk menentukan halaman kode untuk mengidentifikasi kumpulan karakter yang akan digunakan. Ini disimpan dalam format file teks biasa dan berisi informasi tentang pengkodean yang diterapkan untuk membuat shapefile. Jika file CPG tidak tersedia, maka shapefile menggunakan pengkodean default sistem. File CPG, jika ada, harus memiliki awalan yang sama dengan file [SHP](/id/gis/shp/), misalnya, jalan.shp, jalan.cpg.

File CPG dapat dibuka dengan ESRI ArcGIS Pro.

### Format File CPG - Informasi lebih lanjut

Saat melihat shapefile di ArcCatalog atau aplikasi ArcGIS lainnya, Anda hanya melihat shapefile. Namun kenyataannya, shapefile menggunakan file terkait lainnya yang dibaca di samping file shape utama. File CPG juga salah satunya jika ada di samping file SHP utama.

## Referensi

* [Ekstensi file shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

