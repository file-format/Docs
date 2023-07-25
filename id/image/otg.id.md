{
  "date" : "2020-01-10",
  "keywords" :[ "file otg", "format file otg", "apa itu file otg", "file", "contoh otg", "ekstensi file otg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Format File Templat Gambar OpenDocument",
  "description":"Pelajari tentang format file OTG dan API yang dapat membuat dan membuka file OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Apa itu file OTG?

File OTG adalah template gambar yang dibuat menggunakan standar OpenDocument yang mengikuti Aplikasi Office OASIS [spesifikasi 1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Ini mewakili organisasi default dari elemen gambar untuk gambar vektor yang dapat digunakan untuk lebih menyempurnakan konten file. File OTF seperti file berbasis format OpenDocument lainnya yang didasarkan pada format XML untuk mewakili konten dokumen. File OTF dapat dilihat dengan membukanya di teks apa pun atau editor XML standar.

## Spesifikasi Format File OTG ##

Format file OTG didasarkan pada format XML OpenDocument yang memiliki skema mapan. Struktur setiap komponen format OpenDocument diwakili oleh elemen yang memiliki atribut terkait dan umum untuk semua jenis dokumen seperti dokumen teks, spreadsheet, atau file gambar. OTG, sebagai template gambar, secara ekstensif menggunakan spesifikasi Konten Grafik yang meliputi:

* Fitur Halaman yang Disempurnakan untuk Aplikasi Grafis
* Menggambar Bentuk
* Bingkai
* Bentuk 3D
* Bentuk Kustom
* Presentasi Bentuk
* Presentasi Animasi
* Animasi Presentasi SMIL
* Acara Presentasi
* Sajikan Bidang Teks
* Konten Dokumen Presentasi

### Fitur Halaman yang Disempurnakan untuk Aplikasi Grafis ###
#### Master Handout ####

Elemen Master Handout adalah template untuk membuat halaman handout secara otomatis untuk aplikasi yang mendukung pencetakan halaman tersebut.
Atribut yang mungkin terkait dengan `<style:handout-master> ` elemen adalah:

|Tata Letak|Atribut|Deskripsi
---|---|---|
|Tata Letak Halaman Presentasi|presentasi:nama-halaman-presentasi-tata letak|Tautan ke `<style:presentation-page-layout> `atribut
|Tata Letak Halaman|`style:nama-tata letak halaman` | Menentukan tata letak halaman yang berisi ukuran, batas, dan orientasi halaman master handout.
|Page Style|`draw:style-name`|Menetapkan atribut pemformatan tambahan ke halaman master handout dengan menetapkan gaya halaman gambar.|
|Deklarasi Tajuk| `presentasi: gunakan-nama-tajuk`| Menentukan nama deklarasi kolom header yang digunakan untuk semua kolom header yang ditampilkan di halaman master handout.
|Deklarasi Footer| presentation:use-footer-name|Menentukan nama deklarasi bidang footer yang digunakan untuk semua bidang footer yang ditampilkan di halaman master handout.
|Deklarasi Tanggal dan Waktu|use-date-time-name|Menentukan nama deklarasi bidang tanggal-waktu yang digunakan untuk semua bidang tanggal-waktu yang ditampilkan di halaman master handout.

### Menggambar Bentuk ###
Format OpenDocument mendukung beberapa bentuk gambar yang dapat digunakan oleh semua jenis dokumen.

|Bentuk|Atribut Terkait| elemen
---|---|---|
Persegi panjang - `<draw:rect> `|Posisi, Ukuran, Gaya, Lapisan, Indeks-Z, ID, ID Teks, Jangkar teks, latar belakang tabel, posisi ujung gambar, Sudut bulat|Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks
Baris `<draw:line> `|Gaya, Lapisan, Indeks-Z, ID, ID Teks dan Transformasi, Jangkar teks, latar belakang tabel, posisi akhir gambar, Titik awal, Titik Akhir|Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks
Polilin`<draw:polyline> `| Posisi, Ukuran, Kotak tampilan, Gaya, Lapisan, Indeks-Z, ID, ID Teks dan Transformasi, Jangkar teks, latar belakang tabel, posisi ujung gambar, Titik| Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks
Poligon`<draw:polygon> `|Posisi, Ukuran, Kotak tampilan, Gaya, Lapisan, Indeks-Z, ID, ID Teks dan Transformasi, Jangkar teks, latar belakang tabel, posisi akhir gambar, Titik|Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks
|Poligon Biasa `<draw:regular-polygon> `|Posisi, Ukuran, Gaya, Lapisan, Indeks-Z, ID, ID Teks dan Transformasi, Jangkar teks, latar belakang tabel, posisi ujung gambar, Cekung, Sudut, Ketajaman|Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks
|Paht`<draw:path> `|Posisi, Ukuran, Kotak Tampilan, Gaya, Lapisan, Indeks-Z, ID, ID Teks dan Transformasi, Penanda Teks, Latar Belakang Tabel, Posisi Akhir Gambar, Data Jalur| Judul, Deskripsi Panjang, Pendengar Acara, Titik Lem, Teks

### Bingkai ###
Bingkai, dalam dokumen gambar adalah wadah persegi panjang yang berisi kotak teks, gambar, atau objek. Bingkai mendukung fitur tambahan seperti kontur, peta gambar, dan hyperlink. Sebuah bingkai dapat berisi objek dan juga gambar, sehingga memungkinkan untuk memiliki banyak rendisi dari suatu objek. Aplikasi membuat elemen masing-masing berdasarkan dukungan terbaik.

Bingkai dapat berisi:
* Kotak teks
* Objek diwakili baik dalam format OpenDocument atau dalam format biner khusus objek
* Gambar-gambar
* Applet
* Plug-in
* Bingkai mengambang

Sebuah bingkai terkandung dalam dokumen seperti yang ditunjukkan di bawah ini.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referensi ##
* [Format Dokumen Terbuka OASIS untuk Aplikasi Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

