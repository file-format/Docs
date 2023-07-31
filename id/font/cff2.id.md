{
  "date" : "2020-08-20",
  "keywords" :[ "file cff2", "format file cff2", "apa itu file cff2", "file", "contoh cff2", "ekstensi file cff2", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Format File Font Ringkas versi 2",
  "description":"Pelajari tentang Format File CFF2 dan API untuk membuat dan membuka file CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Apa itu file CFF2?

Format file CFF2 adalah versi 2.0 dari format file CFF dan memungkinkan penyimpanan kerangka mesin terbang yang efisien dan metadata yang serupa dengan format file CFF. CFF2 berbeda dari CFF karena dimaksudkan untuk digunakan dalam konteks font OpenType sebagai tabel 'sfnt' dengan tag CFF2. Itu tidak dapat digunakan sebagai program yang berdiri sendiri dan bergantung pada data di tabel OpenType lainnya.

## Format File CFF2

[Spesifikasi format file CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) berisi detail tentang tata letak data internal, tipe data, tabel, dan informasi internal lainnya tentang format file. Itu dapat dirujuk untuk referensi pengembang. Beberapa rincian tentang ini adalah sebagai berikut.

### Tata Letak Data

Data biner format file CFF2 diatur secara logis sebagai sejumlah struktur data terpisah. Tata letak dalam data biner adalah seperti yang ditunjukkan pada tabel berikut.

|Masuk |Komentar|
---|---|
|Tajuk |Lokasi tetap|
|DIK Teratas| Lokasi tetap|
|Global Subr INDEKS| Lokasi tetap|
|Variasi |Toko|
|FDSelect |Tampilkan hanya jika ada lebih dari satu Font DICT dalam Font DICT INDEX.|
|Font DICT INDEX ||
|Array Font DICT| Termasuk dalam Font DICT INDEX.|
|DIK Pribadi| Satu per Font DICT.|

Hanya tiga struktur pertama yang didasarkan pada lokasi tetap. Sisa dicapai melalui offset, dan urutannya dapat diubah.

### Tipe Data

Format file CFF2 menggunakan tipe data berikut.

|Nama |Jangkauan |Deskripsi|
---|---|---|
|uint8 |0 hingga 255 |8-bit nomor tak bertanda|
|uint16 |0 hingga 65535| 16-bit unsigned number|
|uint32 |0 hingga 4294967295| 32-bit unsigned number|
|Offset |bervariasi| 1, 2, 3, atau 4 byte offset (ditentukan oleh bidang OffSize dalam tabel Indeks)|
|OffSize |1 hingga 4| Nomor unsigned 1-byte menentukan ukuran bidang Offset atau bidang |

Ini menyimpan semua data numerik multi-byte dan bidang offset dalam urutan byte big-endian. Format CFF2 bebas dari padding byte karena tidak menghormati batasan penyelarasan apa pun.

### Data DICT

File CFF2 berisi data kamus font sebagai pasangan nilai kunci dalam format token yang ringkas. Kunci kamus dikodekan sebagai operator 1 atau 2 byte dan nilai kamus dikodekan sebagai operan numerik ukuran variabel. Ada tiga struktur yang menggunakan format Data DICT: `Top DICT`, `Font DICT` dan `Private DICT`. Sejumlah tipe operan bilangan bulat dengan berbagai ukuran ditentukan dan dikodekan seperti yang ditunjukkan pada tabel berikut (byte pertama operan adalah b0, byte kedua adalah b1, dan seterusnya).

|Ukuran |b0 rentang |Rentang nilai |Perhitungan nilai|
---|---|---|---|
|1 |32 hingga 246| -107 hingga +107 |b0 - 139|
|2 |247 hingga 250| +108 hingga +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 hingga 254| -1131 hingga -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 hingga +32767| b1 << 8 | b2|
|5 |29| -(2^31) hingga +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Tajuk

Data biner dimulai dengan header yang memiliki format yang ditunjukkan pada Tabel di bawah ini.

|Jenis |Nama |Deskripsi|
---|---|---|
|uint8| versi utama| Format versi mayor. Setel ke 2.|
|uint8| versi minor| Format versi minor. Setel ke nol.|
|uint8| ukuran tajuk| Ukuran tajuk (byte).|
|uint16| topDictLength| Panjang struktur Top DICT dalam byte.|

## Referensi

* [Format File CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

