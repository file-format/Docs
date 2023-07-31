{
  "date" : "2020-08-20",
  "keywords" :[ "file ttf", "format file ttf", "apa itu file ttf", "file", "contoh ttf", "ekstensi file ttf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Format File Font TrueType",
  "description":"TrueType font (TTF) didasarkan pada spesifikasi teknologi font digital yang awalnya dirancang oleh Apple, Inc. Apple dan Microsoft menggunakan TTF pada sistem Operasi Mac dan Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Apa itu file TTF?

File dengan ekstensi .ttf mewakili file font berdasarkan teknologi font spesifikasi TrueType. Ini awalnya dirancang dan diluncurkan oleh Apple Computer, Inc untuk Mac OS dan kemudian diadopsi oleh Microsoft untuk OS Windows. Font TrueType memberikan tampilan kualitas tertinggi pada layar komputer dan printer tanpa bergantung pada resolusi. Semua aplikasi modern yang menggunakan font dapat bekerja dengan file TTF. File font TTF tersedia secara bebas melalui internet dan juga dapat dikonversi ke format file font lain seperti OTF dan WOFF.

## Sejarah Singkat

Dirancang oleh Apply Computer, Inc pada 1980-an untuk MacOS, format font TTF ditujukan untuk menyelesaikan beberapa batasan teknis dengan format Adobe Tipe 1. Apple menyertakan dukungan untuk font TrueType di Mac pada tahun 1991. Tujuan desain di balik font TTF adalah efisiensi dalam penyimpanan dan pemrosesan, serta ekstensibilitas. Berdasarkan ekstensibilitas ini, font yang ada dapat diubah menjadi format TrueType.

Microsoft pertama kali menggunakan font TrueType di Windows 3.1 pada April 1992 setelah Apple setuju untuk melisensikan TrueType ke Microsoft. Ini meningkatkan mekanisme rasterisasi, dan meningkatkan efisiensi dan kinerjanya.

## Spesifikasi Format File Tipe Sejati

File font TrueType adalah file biner yang terdiri dari urutan tabel yang digabungkan. Setiap tabel adalah urutan kata dan memiliki nama yang dikenal sebagai `Tag`. Setiap tag bertipe data uint32 dan terdiri dari empat karakter. Tabel pertama dalam file adalah direktori font yang memberikan akses ke tabel lain dalam file font. Data font terdapat dalam tabel lain yang diikuti setelah tabel direktori font. Karena setiap tabel dapat diakses dengan tagnya, tabel dapat muncul dalam urutan apa pun dalam file.

Tabel yang diperlukan dan nama tagnya ditampilkan pada tabel berikut.

|**Tag**|**Tabel**|
---|---|
|'cmap'| pemetaan karakter ke mesin terbang|
|'glyf'| data mesin terbang|
|'kepala'| tajuk jenis huruf|
|'hehe'| tajuk horizontal|
|'hmtx'| metrik horizontal|
|'loka'| indeks ke lokasi|
|'maksimal'| profil maksimum|
|'nama'| penamaan|
|'postingan'| PostScript|

### Tipe Data
Font TrueType menggunakan bilangan bulat standar dan tipe data tambahan seperti yang tercantum dalam tabel berikut.

|**Tipe Data** | **Deskripsi** |
---|---|
|Frac pendek| pecahan bertanda 16-bit|
|Tetap| Nomor fixed-point bertanda 16,16-bit|
|Kata Kata| Integer bertanda 16-bit yang mendeskripsikan kuantitas dalam FUNits, jarak terukur terkecil dalam ruang em.|
|uFWord| Integer tak bertanda 16-bit yang mendeskripsikan kuantitas dalam FUnits, jarak terukur terkecil dalam ruang em.|
|F2Dot14| Angka tetap bertanda 16-bit dengan 14 bit rendah mewakili pecahan.|
|longDateTime| Format internal yang panjang dari tanggal dalam detik sejak 12:00 tengah malam, 1 Januari 1904. Ini direpresentasikan sebagai bilangan bulat 64-bit yang ditandatangani.|

### Direktori Font

Tabel pertama dalam font TrueType adalah direktori font yang menyediakan akses ke informasi yang diperlukan untuk mengakses data di tabel lain. Lebih lanjut terdiri dari:

* `Offset subtable` - mencatat tabel dalam font dan memberikan informasi offset untuk mengakses setiap tabel dalam direktori
* `Direktori Tabel` - Berisi entri untuk setiap tabel dalam font

#### SubTabel Offset
Subtabel offset ditunjukkan di bawah ini.

|**Jenis**|**Nama**|**Deskripsi**|
---|---|---|
|uint32| tipe scaler| Tag untuk menunjukkan penskalaan OFA yang akan digunakan untuk merasterisasi font ini; lihat catatan pada jenis penskalaan di bawah untuk informasi lebih lanjut.|
|uint16| numTables| jumlah tabel|
|uint16| rentang pencarian| (daya maksimum 2 <= numTables)*16|
|uint16| entrySelektor| log2(daya maksimum 2 <= numTables)|
|uint16| rentangPergeseran| numTables*16-searchRange|

#### Direktori tabel
Direktori tabel muncul tepat setelah subtabel offset. Strukturnya seperti terlihat pada tabel berikut.

|**Jenis**|**Nama**|**Deskripsi**|
---|---|---|
|uint32| tag| pengenal 4-byte|
|uint32| checkSum| checksum untuk tabel ini|
|uint32| mengimbangi| diimbangi dari awal sfnt|
|uint32| panjang| panjang tabel ini dalam byte (panjang sebenarnya bukan panjang empuk)|

Setiap tabel dalam file font harus memiliki entri direktori tabelnya sendiri. Entri dalam tabel harus diurutkan dalam urutan menaik menurut tag.


## Referensi
* [Manual Referensi Font TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Ringkasan TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

