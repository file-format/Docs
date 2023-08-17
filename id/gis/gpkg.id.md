{
  "date" : "2021-07-29",
  "keywords" :[ "file gpkg", "format file gpkg", "apa itu file gpkg", "file", "contoh gpkg", "ekstensi file gpkg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - File Format GeoPackage",
  "description":"Pelajari tentang format file GPKG dan API yang dapat membuat dan membuka file GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Apa itu file GPKG?
File dengan ekstensi .gpkg terdiri dari sistem informasi geografis yang diimplementasikan sebagai wadah database SQLite yang berisi tabel data dan metadata dengan definisi umum, batasan format, pernyataan integritas, dan batasan konten. Itu diterbitkan pada tahun 2014; didefinisikan oleh OGC (Open Geospatial Consortium) atas nama militer AS. Berbagai organisasi pemerintah, komersial, dan sumber terbuka mendukung GeoPackage secara luas.

## format file GPKG
GeoPackage dibuat sebagai file database SQLite 3 yang diperluas; standar mendefinisikan seperangkat aturan (konvensi yang diperlukan) untuk:
- Menyimpan set gambar matriks ubin
- Fitur vektor
- Peta raster pada berbagai skala
- Metadata dan skema

Anda dapat memperluas GeoPackage dengan menggunakan aturan ekstensi sebagaimana didefinisikan dalam pasal 2.3 standar. Tujuan merancang GeoPackage adalah untuk membuat database yang seringan mungkin dan memasukkannya ke dalam file tunggal yang siap digunakan. Ini membuatnya ideal untuk aplikasi seluler dalam mode off-line dan berbagi cepat di penyimpanan cloud atau perangkat penyimpanan USB, dll.

### Isi GPKG
GeoPackages berisi sejumlah tabel, seperti database relasional lainnya. Tabel ini dapat berupa tabel yang ditentukan pengguna atau metadata. GeoPackages terdiri dari dua tabel metadata wajib:

#### gpkg_contents
Daftar isi untuk GeoPackage. Kolom wajib dalam tabel ini adalah:

- **table_name**: nama sebenarnya dari tabel data yang ditentukan pengguna;
- **tipe_data**: tipe data, misalnya judul, fitur, dan atribut;
- **pengidentifikasi dan deskripsi**: teks yang dapat dibaca manusia ;
- **last_change**: tanggal informasi perubahan terakhir, dalam format ISO 8601 ;
- **min_x, min_y, max_x, dan max_y**: luasan spasial konten. ;
- **srs_id**: sistem referensi spasial .

#### gpkg_spatial_ref_sys
Untuk konten referensi spasial; termasuk namun tidak terbatas pada petak dan fitur, setiap baris dalam konten harus mengacu pada sistem referensi koordinat; disimpan di tabel **gpkg_spatial_ref_sys**. Kolom wajib dalam tabel ini adalah:

- **srs_name, description**: nama dan deskripsi yang dapat dibaca manusia untuk SRS;
- **srs_id**: pengidentifikasi unik untuk SRS; juga kunci utama untuk tabel;
- **organisasi**: Nama organisasi yang menentukan tidak peka huruf besar/kecil.
- **organization_coordsys_id**: ID numerik SRS yang ditetapkan oleh organisasi;
- **definisi**: Definisi Teks Terkenal dari SRS.


## Referensi

* [GeoPackage - oleh Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)
* [Memulai Dengan GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

