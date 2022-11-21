{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - Format File Koleksi TrueType",
  "description":"File TrueType Collection (TTC) menggabungkan banyak font menjadi satu file. Apple dan Microsoft menggunakan TTF pada sistem Operasi Mac dan Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Apa itu file TTC?
TTC disingkat TrueType Collection adalah perpanjangan dari format True Type. File TTC dapat menggabungkan beberapa file font ke dalamnya. File-file ini bermanfaat untuk menggabungkan banyak font yang memiliki banyak mesin terbang yang sama. Sebelum Windows 2000, file TTC digunakan dalam versi windows Cina, Jepang, dan Korea tetapi kemudian dukungan tersedia untuk semua wilayah.


## Struktur File Koleksi Font
File TTC terdiri dari tabel Header TTC, Direktori Tabel, dan beberapa tabel OpenType. Header TTC harus ditemukan di awal file. Direktori tabel lengkap untuk setiap font harus ada. Format TableDirectory harus serupa dengan yang ada di file non-koleksi. Jumlah tabel di semua direktori dalam file TTC dihitung dari awal file TTC.
Tabel dalam file TTC direferensikan melalui direktori tabel font masing-masing. Beberapa tabel OpenType harus muncul berkali-kali, satu kali untuk setiap font yang ditambahkan di TTC. Sedangkan tabel lainnya dapat digunakan bersama oleh banyak font di file TTC.

### Tajuk TTC
Sejauh ini tersedia dua versi tabel Header TTC:
- Versi 1.0 digunakan untuk file TTC tanpa tanda tangan digital.
- Versi 2.0 dapat digunakan untuk file TTC dengan atau tanpa tanda tangan digital.
Berikut adalah tabel TTC Header dari kedua versi:

**Tajuk TTC Versi 1.0:**

|Jenis|Nama|Deskripsi|
---|---|---|
|TAG|ttcTag|Font Collection ID string: 'ttcf' (digunakan untuk font dengan garis CFF atau CFF2 serta garis TrueType)|
|uint16|majorVersion|Versi mayor dari TTC Header, = 1.|
|uint16|minorVersion|Versi minor dari TTC Header, = 0.|
|uint32|numFonts|Jumlah font di TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array offset ke TableDirectory untuk setiap font dari awal file|

**Tajuk TTC Versi 2.0:**

|Jenis|Nama|Deskripsi|
---|---|---|
|TAG|ttcTag |String ID Koleksi Font: 'ttcf'|
|uint16| majorVersion |Versi utama dari TTC Header, = 2.|
|uint16| minorVersion |Versi minor dari TTC Header, = 0.|
|uint32| numFonts |Jumlah font di TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Array offset ke TableDirectory untuk setiap font dari awal file|
|uint32| dsigTag |Tag menunjukkan bahwa ada tabel DSIG, 0x44534947 ('DSIG') (null jika tidak ada tanda tangan)|
|uint32| dsigLength |Panjang (dalam byte) dari tabel DSIG (nol jika tidak ada tanda tangan)|
|uint32| dsigOffset |Offset (dalam byte) dari tabel DSIG dari awal file TTC (nol jika tidak ada tanda tangan)|

## Referensi
* [File Font OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

