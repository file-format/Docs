{
  "date" : "2020-08-20",
  "keywords" :[ "file otf", "format file otf", "apa itu file otf", "file", "contoh otf", "ekstensi file otf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Format File Font TrueType",
  "description":"Pelajari tentang format file OTF dan API yang dapat membuat dan membuka file OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Apa itu file OTF?

File dengan ekstensi .otf mengacu pada format font OpenType. Format font OTF lebih terukur dan memperluas fitur format [TTF](/id/font/ttf/) yang ada untuk tipografi digital. Dikembangkan oleh Microsoft dan Adobe, OTF menggabungkan fitur format font PostScript dan TrueType. Hal ini membuat format OTF mengakomodasi sebagian besar sistem penulisan dan oleh karena itu digunakan secara seragam pada platform komputer utama. Format font OpenType didukung oleh Mac OS X dan Windows 2000 dan yang lebih baru.

## Sejarah Singkat

Persyaratan font OpenType berasal dari persyaratan untuk format font yang lebih ekspresif yang dapat menangani tipografi yang halus. Selain itu, ini ditujukan untuk memenuhi persyaratan perilaku kompleks dari banyak sistem penulisan dunia. Microsoft berusaha melisensikan teknologi tipografi canggih Apple, yang dikenal sebagai Tipografi GX, pada awal 1990-an. Ini tidak berjalan dengan baik dan sebagai hasilnya, Microsoft mulai meningkatkan teknologi font TrueType miliknya pada tahun 1994. Modifikasi juga termasuk untuk memperkenalkan format font yang lebih cocok yang juga memenuhi fitur format font Adobe Type 1 (PostScript).

Adobe, pada tahun 1996, bergabung dengan Microsoft dalam upayanya untuk menggantikan format font TrueType Apple dan Type 1 miliknya sendiri. Ini menghasilkan kombinasi dari kedua format font dasar untuk mengatasi keterbatasan dan menambahkan ekstensi baru. Teknologi baru ini diperkenalkan pada tahun yang sama dengan nama **OpenType**.

## Spesifikasi Format File OTF

Spesifikasi OTF tersedia untuk umum oleh Microsoft dan dapat dirujuk dari perspektif pengembang. Seperti TTF, ini menggunakan struktur kontainer 'sfnt' yang sama dan kompatibel dengan spesifikasi TrueType. Data di dalam file font OpenType digunakan untuk tujuan yang berbeda seperti menghitung tata letak teks, mendefinisikan glyph sebagai garis TrueType atau Compact Font Format (CFF), memberikan bitmap monokromatik atau berwarna atau dokumen SVG sebagai deskripsi glyph alternatif, dan informasi meta-data.

### Tipe Data OTF
File OTF menggunakan tipe data berikut yang semuanya ada di Big Endian.

|Tipe Data| Deskripsi|
---|---|
|uint8| 8-bit unsigned integer.|
|int8| Bilangan bulat bertanda 8-bit.|
|uint16| Bilangan bulat tak bertanda 16-bit.|
|int16| Bilangan bulat bertanda 16-bit.|
|uint24| 24-bit unsigned integer.|
|uint32| Bilangan bulat tak bertanda 32-bit.|
|int32| Bilangan bulat bertanda 32-bit.|
|Tetap| nomor fixed-point bertanda 32-bit (16.16)|
|FWORD| int16 yang mendeskripsikan kuantitas dalam unit desain font.|
|UFWORD| uint16 yang mendeskripsikan kuantitas dalam unit desain font.|
|F2DOT14| Angka tetap bertanda 16-bit dengan pecahan 14 bit rendah (2,14).|
|LONGDATETIME| Tanggal dan waktu direpresentasikan dalam hitungan detik sejak 12:00 tengah malam, 1 Januari 1904, UTC. Nilai direpresentasikan sebagai bilangan bulat 64-bit bertanda.|
|Tag| Larik empat uint8 (panjang = 32 bit) digunakan untuk mengidentifikasi tabel, sumbu variasi desain, skrip, sistem bahasa, fitur, atau garis dasar|
|Offset16| Offset pendek ke tabel, sama seperti uint16, offset NULL = 0x0000|
|Offset32| Offset panjang ke tabel, sama seperti uint32, offset NULL = 0x00000000|
|Versi16Dot16| Dikemas nilai 32-bit dengan nomor versi mayor dan minor. (Lihat Nomor Versi Tabel.)|

### Direktori Tabel OTF

File OTF dimulai dengan direktori tabel. Direktori ini adalah kumpulan tabel tingkat atas dalam file font. Bergantung pada jumlah font dalam file, direktori tabel mungkin terletak di lokasi berbeda dalam file. Misalnya, jika file font hanya memiliki satu font, direktori tabel dimulai pada byte 0 dari file tersebut. Dalam hal beberapa koleksi OpenType Fonts,
awal direktori tabel ditunjukkan di TTCHeader.

|Jenis |Nama |Deskripsi|
---|---|---|
|uint32 |sfntVersion| 0x00010000 atau 0x4F54544F ('OTTO')|
|uint16| numTables |Jumlah tabel.|
|uint16| searchRange |Daya maksimum 2 kurang dari atau sama dengan numTables, dikalikan 16 ((2\**floor(log2(numTables))) * 16, di mana “**” adalah operator eksponensial).|
|uint16 |entrySelector Log2 dengan daya maksimum 2 kurang dari atau sama dengan numTables (log2(searchRange/16), yang sama dengan floor(log2(numTables))).|
|uint16 |rangeShift |numTables kali 16, minus searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Larik catatan tabel—satu untuk setiap tabel tingkat atas dalam font|


### Catatan Tabel

Untuk setiap tabel tingkat teratas dalam font, terdapat Catatan Tabel yang terdiri dari bidang-bidang berikut.

|Tipe| Nama| Deskripsi|
---|---|---|
|Tag| tableTag| Pengidentifikasi tabel.|
|uint32| checksum| Checksum untuk tabel ini.|
|Offset32| mengimbangi| Offset dari awal file font.|
|uint32| panjang Panjang tabel ini.|

Setiap tabel dalam file font OpenType diwakili oleh nama yang dikenal sebagai tag tabel. Semua catatan dalam larik harus diurutkan dalam urutan menaik berdasarkan tag.

## Referensi
* [Spesifikasi Font OpenType oleh Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [Ringkasan TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

