{
  "date" : "2021-01-21",
  "keywords" :[ "file ai", "format file ai", "apa itu file ai", "file", "contoh ai", "ekstensi file ai", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - File Karya Seni Adobe Illustrator",
  "description":"Pelajari tentang format file AI dan API yang dapat membuat dan membuka file AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Apa itu file AI?

File dengan ekstensi .ai adalah file Karya Seni Adobe Illustrator yang berisi grafik vektor dalam satu halaman. ia menggunakan titik untuk membuat jalur untuk menampilkan data gambar, sehingga aman dari kehilangan kualitas gambar jika diperbesar. Format file AI didasarkan pada format file PGF yang mirip dengan file AI. Format AI menemukan penggunaan utamanya untuk logo dan media cetak, dan versi awalnya dianggap serupa dengan file [EPS](/id/image/eps/). File AI dapat dibuka dengan alat Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, dan CorelDraw Graphics.

## Format File AI

AI adalah format file milik Adobe Illustrator dan menggunakan pendekatan jalur ganda yang mirip dengan PGF untuk menyimpan file yang kompatibel dengan EPS. [Spesifikasi Format File Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) memberikan detail referensi pengembang untuk detail internal format file ini. Semua dokumen (file) yang dibuat oleh Adobe Illustrator adalah dokumen berbahasa PostScript dan memiliki dua bagian utama yang sesuai dengan Konvensi Penataan Dokumen: `prolog` dan `script`.

### Prolog

Bagian prolog merangkum informasi yang diperlukan untuk interpretasi file. Contohnya adalah kotak pembatas yang berisi semua tanda pada halaman. Ini juga berisi informasi sumber daya seperti font dan definisi prosedur. Sumber daya ini secara logis dikelompokkan ke dalam set yang disebut procsets dan berisi metode eksplisit untuk menginisialisasi dan mengakhiri prosedur mereka.

### Skrip

Elemen grafik pada halaman dijelaskan oleh skrip. Skrip berisi referensi ke operator dan prosedur di prolog, bersama dengan operan dan data. Tiga bagian logis dari skrip meliputi:

* Urutan Pengaturan - yang menginisialisasi dan mengaktifkan sumber daya yang ditentukan dalam prolog
* Urutan operator deskriptif
* Cuplikan yang menonaktifkan sumber daya

Operator dalam skrip adalah urutan elemen grafik yang ditulis dalam bahasa yang ditentukan oleh procset di prolog. Urutan ini terdiri dari kumpulan elemen data, definisi atribut grafis, dan panggilan ke prosedur yang didefinisikan dalam procsets.

### Tag Objek

Tag objek digunakan untuk melampirkan informasi khusus ke objek seni Adobe Illustrator. Tag terdiri dari:

* Tanda pengenal
* Jenis label
* Data

## Referensi
* [Spesifikasi Format File Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Format File AI oleh PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

