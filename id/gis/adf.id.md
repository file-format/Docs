{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo Format Kotak Biner",
  "description":"Pelajari tentang format file ADF dan API yang dapat membuat dan membuka file ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Apa itu file ADF?

File dengan ekstensi .adf adalah format file data raster yang digunakan oleh aplikasi perangkat lunak ESRI seperti ArcGIS, ArcView, dan ArcInfo. Data spasial disimpan sebagai kisi biner yang asli ESRI. Kisi terdiri dari baris dan kolom sel yang dapat berupa bilangan bulat maupun titik mengambang. Kisi bilangan bulat dalam file ADF mewakili data diskrit dan kisi titik-mengambang mewakili data kontinu. Format file ESRI populer lainnya adalah file [SHP](/id/gis/shp/) yang merepresentasikan informasi Geospasial dalam bentuk data vektor untuk digunakan oleh aplikasi Sistem Informasi Geografis (SIG).

## Format File ADF - Informasi Lebih Lanjut

File ADF disimpan sebagai file biner ke disk dalam kotak biner. Kisi bilangan bulat memiliki atribut yang disimpan dalam tabel atribut nilai (PPN). Setiap nilai unik dalam kisi memiliki satu catatan dalam PPN tempat catatan menyimpan nilai unik dan jumlah sel dalam kisi diwakili oleh nilai tersebut.

Kisi titik apung tidak memiliki PPN.

### Struktur Kisi

Di dalam file ADF, kisi-kisi diimplementasikan menggunakan struktur data raster ubin. Unit dasar di dalam struktur data raster ini adalah blok sel persegi panjang. Setiap blok disimpan pada disk dan dikompresi dalam struktur file dengan panjang variabel, yang disebut ubin. Setiap blok disimpan sebagai satu record dengan panjang variabel.

Raster GRID disimpan di ruang kerja, di mana ruang kerja berisi satu subdirektori info dan subdirektori untuk setiap GRID. Ada beberapa file lokasi geografis dan atribut data untuk grid yang sesuai. Subdirektori Info berisi beberapa file yang menyimpan informasi tertentu tentang GRID dan kumpulan data lainnya, seperti cakupan, di ruang kerja.

## Referensi ##

* [Format Petak ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
