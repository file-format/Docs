{
  "date" : "2019-10-11",
  "keywords" :[ "file shp", "format file shp", "apa itu file shp", "file", "contoh shp", "ekstensi file shp", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - Berkas Bentuk ESRI",
  "description":"Pelajari tentang format file SHP dan API yang dapat membuat dan membuka file SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file SHP?

SHP adalah ekstensi file untuk salah satu jenis file utama yang digunakan untuk representasi ESRI Shapefile. Ini mewakili informasi Geospasial dalam bentuk data vektor untuk digunakan oleh aplikasi Sistem Informasi Geografis (SIG). Formatnya telah dikembangkan sebagai spesifikasi terbuka untuk memfasilitasi interoperabilitas antara ESRI dan produk perangkat lunak lainnya.

## Representasi data

Seperti disebutkan, format shapefile menggambarkan informasi geospasial dari kumpulan data sebagai fitur vektor. Ciri-ciri vektor tersebut antara lain:

* poin
* baris
* poligon

Fitur-fitur ini dalam kombinasi dapat mewakili hampir semua jenis bentuk seperti sumur air, batas negara, titik spasial, aliran sungai, danau, dll. Setiap fitur vektor dapat memiliki atribut yang benar-benar menentukan tujuan dari fitur tersebut. Sebagai contoh, sebuah shapefile yang berisi kota-kota di Los Angeles dapat memiliki nama kota dan suhu sebagai atribut yang memberikan representasi yang bermakna pada data spasial.

## File Terkait

File shp mandiri tidak dapat digunakan oleh aplikasi perangkat lunak untuk mengartikan data yang dikandungnya. Untuk memahami informasi yang terkandung dalam file seperti itu, sebuah shapefile memanfaatkan file wajib tambahan berikut.

* file shx - file indeks
* File dbf - file dBASE yang menyimpan semua atribut bentuk di file utama
* file prj - menyimpan informasi proyek dari file tersebut

Mungkin ada file opsional lain yang memiliki nama yang sama dengan file utama.

## Spesifikasi Format File SHP

Spesifikasi terbuka shapefile tersedia online dari ESRI dalam bentuk [Deskripsi Teknis](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) dan menguraikan struktur keseluruhan file secara mendetail. Informasi dalam file .shp utama terdiri dari header dan record. Header file dengan panjang tetap diikuti oleh record dengan panjang variabel di mana setiap record terdiri dari header record dengan panjang tetap diikuti oleh isi record dengan panjang variabel.

### Header Berkas SHP Utama

File Header utama dimulai dari awal file dan panjangnya 100 byte. Organisasi header file utama ini beserta posisi, nilai, jenis, dan urutan byte byte adalah seperti yang ditunjukkan pada tabel berikut.


|Bytes|Bidang|Nilai|Jenis|Urutan Byte
---|---|---|---|---|
|0-3|Kode File|9994|Integer|Big Endian
|4-23|Tidak terpakai|0|Bilangan Bulat|Big Endian
|24-27|Panjang File|Panjang File|Integer|Big Endian
|28-31|Versi|1000|Integer|Little Endian
|32-35|Tipe Bentuk|Tipe Bentuk|Integer|Little Endian
|36-67|Persegi Panjang Batas Minimum|Xmin, Ymin, Xmax, dan Ymax|ganda|Little Endian
|68-83|Bounding Box|Zmin, Zmax|double|Little Endian
|84-99|Kotak Pembatas|Mmin, Mmax|ganda|

Perlu dicatat bahwa nilai panjang file adalah total panjang file dalam kata 16-bit yang juga mencakup lima puluh kata 16-bit yang membentuk header.

#### Jenis Bentuk

Nilai-nilai bidang tipe bentuk pada tabel di atas adalah sebagai berikut:


|Nilai|Jenis Bentuk
---|---|
|0|Bentuk Null
|1|Titik
|3|Poliline
|5|Poligon
|8|MultiPoin
|11|TitikZ
|13|PolyLineZ
|15|PoligonZ
|18|MultiPointZ
|21|PoinM
|23|PolyLineM
|25|PoligonM
|28|MultiPointM
|31|MultiPatch

### Rekaman Data ###

Header file utama diikuti oleh record dengan panjang variabel di mana setiap record terdiri dari header record dengan panjang tetap diikuti oleh isi record dengan panjang variabel.

#### Tajuk Rekam ####

Header rekaman berisi informasi tentang nomor rekaman dan panjang isi rekaman dengan panjang tetap 8 byte. Organisasi tajuk rekaman adalah seperti yang ditunjukkan berikut:


|Bytes|Bidang|Nilai|Jenis|Urutan Byte
---|---|---|---|---|
|0-3|Rekam Nomor|Rekam Nomor|Integer|Besar
|4-7|Rekam Panjang|Rekam Panjang|Bilangan Bulat|Besar

#### Rekam Isi ####

Isi record shapefile terdiri dari tipe bentuk yang diikuti oleh data geometris untuk bentuk tersebut. Tipe bentuk 0 mewakili bentuk nol yang tidak memiliki data geometris untuk bentuk tersebut. Panjang isi rekaman merupakan cerminan dari bagian bentuk dan simpul. Mari kita ambil contoh tipe Point Shape untuk menguraikan bagaimana record berisi informasi tentang tipe bentuk seperti itu.

Suatu titik mewakili lokasi geografis tertentu dalam urutan X,Y di mana setiap koordinat diwakili oleh nilai presisi ganda. Tabel berikut menunjukkan susunan tipe bentuk Titik.


|Bytes|Jenis Bentuk|Nilai|Jenis|Nomor|Urutan Byte
---|---|---|---|---|---|
|0-3|Jenis Bentuk|1|Integer|1|Kecil
|4-11|X|X|ganda|1|Sedikit
|12-19|Y|Y|ganda|1|Sedikit

Contoh jenis bentuk lainnya dapat ditemukan di dokumen deskripsi teknis ESRI.

## Referensi ##

* [Deskripsi Teknis ESRI Shapefile](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) oleh ESRI

