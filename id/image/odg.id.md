{
  "date" : "2019-10-11",
  "keywords" :[ "file odg", "format file odg", "apa itu file odg", "file", "contoh odg", "ekstensi file odg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File ODG",
  "description":"Pelajari tentang format file ODG dan API yang dapat membuat dan membuka file ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ODG?

Format file ODG digunakan oleh aplikasi Draw Apache OpenOffice untuk menyimpan elemen gambar sebagai gambar vektor. Ini mengikuti spesifikasi format file berbasis XML yang digariskan oleh Kemajuan Standar Informasi Struktural (OASIS). ODG merepresentasikan gambar sebagai gambar vektor menggunakan titik, garis, dan kurva. Selain OpenOffice, LibreOffice dan aplikasi lain juga memberikan dukungan untuk bekerja dengan format file ODG. Format lain yang didukung oleh OpenOffice, misalnya, termasuk [ODT](/id/word-processing/odt/), ODF, [ODP](/id/presentation/odp/) dan [ODS](/id/spreadsheet/ods/).


## Spesifikasi Format File ODG

Format file ODG didasarkan pada format OpenDocument yang merupakan format dokumen XML terstruktur dengan skema yang terdefinisi dengan baik.
Setiap komponen struktural dari format OpenDocument diwakili oleh elemen yang memiliki atribut terkait. Struktur berbasis XML adalah umum untuk semua jenis dokumen seperti dokumen teks, spreadsheet, atau file gambar. Sebuah dokumen dapat berisi gaya yang berbeda. Struktur file OpenDocument terdiri dari elemen-elemen berikut.
* Akar Dokumen
* Dokumen MetaData
* Elemen Tubuh dan tipe Dokumen
* Pengaturan aplikasi
* Skrip
* Deklarasi Wajah Font
* Gaya
* Gaya dan Tata Letak Halaman

## Akar Dokumen ##

Elemen root dokumen berisi seluruh dokumen dan merupakan elemen utama file dalam format OpenDocument. Jenis elemen root dokumen yang sama berlaku untuk semua jenis dokumen seperti teks, dokumen, spreadsheet, dan dokumen gambar.

### Elemen Akar ###
Satu dokumen XML diwakili oleh elemen akarnya sendiri. Lima elemen root pendukung yang berbeda adalah sebagai berikut.

`<office:document>` - Lengkapi dokumen kantor dalam satu dokumen XML.
`<office:document-content>` - Konten dokumen dan gaya otomatis yang digunakan dalam konten.
`<office:document-styles>` - Gaya yang digunakan dalam konten dokumen dan gaya otomatis yang digunakan dalam gaya itu sendiri.
`<office:document-meta>` - Mendokumentasikan informasi meta, seperti penulis atau waktu tindakan penyimpanan terakhir.
`<office:document-settings>` - Pengaturan khusus aplikasi, seperti ukuran jendela atau informasi printer.

### MetaData Dokumen ODG ###
OpenDocument berisi semua elemen metadata di \<office:meta> elemen. Informasi umum tentang dokumen ini dimuat di awal dokumen dan aplikasi dapat memperbarui banyak contoh dari elemen yang sama.

### Elemen Badan dan Tipe Dokumen ###
Badan dokumen menunjukkan jenis konten yang terkandung dalam dokumen menggunakan elemen tipe dokumen. Jenis dokumen ini adalah:
* dokumen teks
* menggambar dokumen
* dokumen presentasi
* dokumen spreadsheet
* dokumen grafik
* dokumen gambar

### Pengaturan aplikasi ###
Pengaturan untuk aplikasi kantor mewakili pengaturan berbeda yang terkait dengan konfigurasi dokumen atau tampilan visual dokumen. Setiap kategori diwakili oleh `<config:config-item-set>`. Contoh kategori pengaturan tersebut meliputi:
* Pengaturan dokumen misalnya printer default
* Lihat Pengaturan misalnya tingkat zoom

### Skrip ###
Biasanya dokumen berisi beberapa skrip. Setiap skrip dalam file OpenDocument diwakili oleh `<office:script>`elemen. Elemen skrip ini terkandung dalam satu `<office:scripts>`elemen. Skrip tidak memperbarui dokumen saat dokumen sedang dimuat.
### Deklarasi Wajah Font ###

Deklarasi bentuk font berisi informasi tentang font yang digunakan oleh pembuat dokumen. Informasi ini membantu menemukan font ini di sistem lain.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Gaya ###
Gaya berikut didukung oleh format OpenDocument.

`Common Styles` - Representasi XML dari gaya tersebut disebut sebagai gaya
`Gaya Otomatis` - Berisi properti pemformatan yang, dalam tampilan antarmuka pengguna dokumen, ditetapkan ke objek seperti paragraf.
`Mater Styles` - gaya umum yang berisi informasi pemformatan dan konten tambahan yang ditampilkan dengan konten dokumen saat gaya diterapkan. Contoh gaya master adalah halaman master.

## Referensi ##
* [Format Dokumen Terbuka OASIS untuk Aplikasi Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

