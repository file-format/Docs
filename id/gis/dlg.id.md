{
  "date" : "2021-07-30",
  "keywords" :[ "file dlg", "format file dlg", "apa itu file dlg", "file", "contoh dlg", "ekstensi file dlg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Format Indeks Bentuk Shapefile",
  "description":"Pelajari tentang format file DLG dan API yang dapat membuat dan membuka file DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Apa itu file DLG?
File dengan ekstensi .dlg berisi Digital Line Graph yang merupakan fitur peta kartografi yang ditampilkan dalam bentuk vektor digital yang dikelola oleh US Geological Survey (USGS). File DLG tersedia dalam dua format berbeda:
1. **Format opsional**: Format yang mudah digunakan yang menggabungkan panjang rekaman logis 80 byte, sistem koordinat dasar UTM, dan keterkaitan topologi yang terdapat dalam elemen garis, simpul, dan area.
2. **Format Standar Transfer Data Spasial (SDTS)**: format yang memfasilitasi transfer data spasial antar sistem komputer yang berbeda.

## Format File DLG
Format file DLG dirancang untuk peta USGS dan ditransmisikan dalam skala besar, menengah, dan kecil hingga sembilan kategori fitur yang berbeda. File DLG tersedia dalam format opsional dan Standar Transfer Data Spasial (SDTS) yang memiliki struktur topologi untuk digunakan dalam pemetaan dan aplikasi GIS.
### Spesifikasi Format File DLG
File DLG didistribusikan pada tiga skala berbeda:

1. **Skala besar** - biasanya terkait dengan:
- USGS 7,5- dengan 7,5 menit
- Seri peta segi empat topografi skala 1:24.000 dan 1:25.000
- Skala 1:63.360 untuk Alaska
- Skala 1:30.000 untuk Puerto Rico
 

2. **Skala menengah** - berasal dari USGS:

- 30- dengan 60 menit

- Seri peta skala 1:100.000
3. **Skala kecil** - berasal dari peta penampang USGS skala 1:2.000.000 dari Atlas Nasional Amerika Serikat
### Kategori Data
Sembilan kategori lapisan, atau fitur yang berbeda, tersedia dalam file DLG:
1. Sistem Survei Tanah Umum (PLSS)
2. Batasan (BD)
3. Transportasi (TR)
4. Hidrografi (HY)
5. Hipografi (HP)
6. Fitur non-vegetatif (NV)
7. Kontrol dan penanda survei (SM)

8. Fitur Buatan Manusia (MS)

9. Tutupan permukaan vegetatif (SC)

File DLG skala besar menawarkan kesembilan lapisan, sedangkan skala menengah menawarkan lima lapisan PLSS, BD, TR, HY, dan HP. DLG skala kecil menawarkan lima lapisan PLSS, BD, TR, HY, dan MS.

## Referensi

* [Grafik garis digital - oleh Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


