{
  "date" : "2021-02-25",
  "keywords" :[ "file bdf", "format file bdf", "apa itu file bdf", "file", "contoh bdf", "ekstensi file bdf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Format Distribusi Glyph Bitmap",
  "description":"Pelajari tentang format file BDF dan API yang dapat membuat dan membuka file BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Apa itu file BDF?
File BDF adalah bentuk yang dapat dibaca manusia dan biasanya didistribusikan dalam pengkodean ASCII. File dimulai dengan informasi global yang relevan dengan font lengkap, diikuti dengan informasi dan bitmap untuk mesin terbang individu. Data di dalamnya menunjukkan font untuk orientasi ukuran tunggal. Metrik yang digunakan di lebih dari satu arah dapat terdiri dari satu file. Dalam file BDF, setiap item dimuat pada baris teks terpisah di dalam file. Spasi digunakan untuk memisahkan item pada baris.

## format file BDF
BDF singkatan dari Glyph Bitmap Distribution Format; dimiliki oleh Adobe adalah format file untuk menyimpan font jenis bitmap. Konten tersebut berbentuk file teks yang dimaksudkan untuk dapat dibaca oleh komputer dan manusia. BDF terutama digunakan di lingkungan Unix X Window. Itu telah digantikan secara luas oleh format font PCF yang dianggap lebih efisien, dan oleh font OpenType dan TrueType.
### struktur file BDF
File font BDF terdiri dari tiga bagian:

- bagian global yang berlaku untuk semua mesin terbang dalam font.
- bagian dengan entri terpisah untuk setiap mesin terbang.
- pernyataan ENDFONT.

## Contoh
Berikut adalah contoh font yang mengandung satu mesin terbang, untuk huruf besar ASCII 'A'. Deklarasi globalnya dimulai dengan baris "STARTFONT" dan diakhiri dengan baris "CHARS".
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Referensi
* [Format Distribusi Bitmap Glyph](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Spesifikasi Glyph Bitmap Distribution Format (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

