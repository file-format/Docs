{
  "date" : "2020-08-20",
  "keywords" :[ "file cff", "format file cff", "apa itu file cff", "file", "contoh cff", "ekstensi file cff", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Format File Font Ringkas",
  "description":"Pelajari tentang Format File CFF dan API untuk membuat dan membuka file CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Apa itu file CFF?

File dengan ekstensi .cff adalah Compact Font Format dan juga dikenal sebagai PostScript Type 1, atau CIDFont. CFF bertindak sebagai wadah untuk menyimpan banyak font bersama dalam satu unit yang dikenal sebagai FontSet. Desain font CFF memungkinkan penyematan kode bahasa PostScript yang memungkinkan fleksibilitas tambahan dan ekstensibilitas format untuk penggunaan dengan lingkungan printer. File font CFF dapat dibuka dan dikonversi menggunakan API seperti [Aspose.Font](https://products.aspose.com/font).

## Format File CFF

File CFF adalah file biner yang berisi tata letak data terstruktur, memiliki tipe data yang ditentukan, header, organisasi mesin terbang, dan kamus tabel. Detail selengkapnya tentang ini dapat ditemukan di [spesifikasi format font ringkas](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Tata Letak Data
Tata letak data format file CFF adalah seperti yang ditunjukkan di bawah ini.

|Masuk|Komentar|
---|---|
|Tajuk|–|
|NamaINDEX|–|
|INDEKS DICT Teratas|–|
|INDEKS RANGKAIAN|–|
|INDEKS Bawah Tanah Global|–|
|Encoding–Charsets|–|
|FDSelect|CIDFonts saja|
|CharStrings INDEX|per-font|
|Font DICT INDEX|per-font, hanya CIDFonts|
|DICT Pribadi|per-font|
|INDEKS Subr Lokal|DICT per-font atau per-Pribadi untuk CIDFonts|
|Pemberitahuan Hak Cipta dan Merek Dagang|–|

### Tipe Data

Tipe data CFF adalah seperti yang ditunjukkan pada tabel berikut.

|Nama|Jangkauan|Deskripsi|
---|---|---|
|Card8|0 –255|1-byte unsigned number|
|Kartu16|0 – 65535|nomor tak bertanda 2-byte|
|Offset|bervariasi|1, 2, 3, atau 4 byte offset (ditentukan oleh bidang OffSize)|
|OffSize|1–4|1-byte unsigned number menentukan ukuran dari satu atau beberapa field Offset|
|SID|0 – 64999|pengidentifikasi string 2-byte|

### Tajuk

Data biner dimulai dengan header yang memiliki format yang ditunjukkan pada tabel berikut.

|Jenis|Nama|Deskripsi|
---|---|---|
|Card8|mayor|Format versi mayor (mulai dari 1)|
|Card8|minor|Format versi minor (mulai dari 0)|
|Kartu8|Ukuran hdr| Ukuran tajuk (byte)|
|OffSize|offSize|Ukuran ofset mutlak (0)|

## Referensi

* [Tabel Format Font Ringkas](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [Format File CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Set Bagan CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

