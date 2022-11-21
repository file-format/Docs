{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "file", "ekstensi", "format file", "File Interchange Data", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Panduan format file Anda untuk mengetahui apa itu ekstensi file DIF dan API yang dapat membuat dan membuka file DIF.",
  "title" :"DIF - Format File Pertukaran Data",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file DIF?

DIF adalah singkatan dari Data Interchange Format yang digunakan untuk mengimpor/mengekspor data spreadsheet antara aplikasi yang berbeda. Ini termasuk Microsoft Excel, OpenOffice Calc, StarCalc dan banyak lainnya. Ini menyimpan data yang terkandung dalam satu spreadsheet yang merupakan satu-satunya batasan format file ini.

## Sejarah Singkat Format File DIF ##

Format file DIF dikembangkan oleh Software Arts, Inc. pada awal 1980-an. Spesifikasi format file untuk DIF disertakan dalam VisiCalc yang merupakan program spreadsheet pertama untuk komputer pribadi. Spesifikasi ini memiliki hak cipta pada tahun 1981 dan merupakan merek dagang terdaftar dari Software Arts Products Corp.

## Format File DIF ##

DIF menyimpan konten spreadsheet dalam file teks ASCII yang memungkinkannya untuk dilihat dan diedit dengan editor teks. Format memiliki tempatnya dalam daftar format serialisasi data untuk karakteristik pertukaran datanya. File DIF terdiri dari 2 bagian; header dan data.

Segala sesuatu di DIF diwakili oleh potongan 2 atau 3 baris. Header mendapatkan potongan 3 baris; data, 2.

* Potongan header dimulai dengan pengidentifikasi teks yang semuanya menggunakan huruf besar, hanya karakter alfabet, dan kurang dari 32 huruf. Baris berikutnya harus sepasang angka, dan baris ketiga harus berupa string yang dikutip.
* Potongan data dimulai dengan pasangan angka dan baris berikutnya adalah string yang dikutip atau kata kunci.

### Nilai ###

Nilai menempati dua baris, yang pertama adalah sepasang angka dan yang kedua berupa string atau kata kunci. Angka pertama dari pasangan menunjukkan jenis:

* −1 – tipe direktif, angka kedua diabaikan, baris berikut adalah salah satu dari kata kunci ini:
** BOT – awal tupel (awal baris)
** EOD – akhir data
* 0 – tipe numerik, nilai adalah angka kedua, baris berikut adalah salah satu dari kata kunci ini:
** V – valid
** NA – tidak tersedia
** KESALAHAN – kesalahan
** BENAR – nilai boolean sebenarnya
** FALSE – nilai boolean salah
* 1 – tipe string, angka kedua diabaikan, baris berikutnya adalah string dalam tanda kutip ganda

### Potongan Header DIF ###

Potongan header file DIF terdiri dari baris pengidentifikasi diikuti oleh dua baris nilai. Nilai numerik dalam potongan header hanya menggunakan string kosong, bukan kata kunci validitas. Rincian potongan tajuk ini adalah sebagai berikut.

* TABEL - nilai numerik mengikuti versi, baris kedua yang tidak digunakan dari nilai berisi komentar generator
* VEKTOR - jumlah kolom mengikuti sebagai nilai numerik
* TUPLES - jumlah baris mengikuti sebagai nilai numerik
* DATA - setelah nilai numerik dummy 0, data untuk tabel mengikuti, setiap baris didahului oleh nilai BOT, seluruh tabel diakhiri dengan nilai EOD

### Contoh DIF ###

Contoh berikut memperlihatkan konten lembar kerja sederhana dan representasi DIF yang setara.


|Nama|Usia
---|---|
|Bob|34
|Lembaran|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referensi ##

* [ DIF - Oleh Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

