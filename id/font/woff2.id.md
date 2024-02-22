{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "File WOFF2 - File Format Font Terbuka Web 2.0",
  "description": "Pelajari tentang apa itu file WOFF2 dan API yang dapat membuat dan membuka file WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-id2"
}
},
  "lastmod": "2023-01-10"
}

## Apa itu berkas WOFF2?

WOFF2 adalah format file font yang merupakan versi lebih terkompresi dari Web Open Font Format (WOFF). Ini dikembangkan sebagai cara untuk mengurangi ukuran file font web, memungkinkannya memuat lebih cepat dan menggunakan lebih sedikit bandwidth. WOFF2 menggunakan algoritme kompresi yang disebut Brotli untuk mengompresi data font, yang dapat menghasilkan ukuran file yang jauh lebih kecil dibandingkan font [WOFF](/font/woff/) yang setara. Format ini didukung oleh sebagian besar browser web modern termasuk Chrome, Firefox, Safari, Opera, dan Edge (versi 14 dan seterusnya).

## Format File WOFF2 - Informasi Lebih Lanjut

Struktur file internal file font WOFF2 terdiri dari beberapa bagian berbeda, termasuk header, metadata, direktori tabel, dan data font itu sendiri.

 1. Header berisi informasi tentang format file secara keseluruhan, termasuk nomor versi dan jumlah tabel yang ada dalam file.

 1. Bagian metadata berisi informasi seperti nama font, hak cipta, dan informasi terkait font lainnya.

 1. Direktori tabel berisi informasi tentang berbagai tabel yang membentuk font, termasuk lokasinya dalam file dan panjangnya.

 1. Data font itu sendiri dibagi menjadi beberapa tabel berbeda, yang masing-masing berisi informasi spesifik tentang font, seperti karakternya dan mesin terbangnya yang sesuai. Tabel ini mungkin mencakup:

 * Tabel 'glyf' berisi garis besar font sebenarnya, termasuk bentuk dan ukuran setiap karakter.
 * Tabel 'head' berisi informasi umum tentang font, seperti nomor versi, ukuran desain, dan sebagainya.
 * Tabel 'hmtx' berisi informasi tentang metrik font, termasuk lebar dan posisi karakter.
 * Setiap tabel dikompresi dan disimpan dalam format file WOFF2 setelah proses pengkodean selesai.

Struktur keseluruhannya dirancang untuk memungkinkan penguraian dan penguraian kode dengan cepat, sehingga browser web dapat memuat dan menampilkan font dengan cepat dan efisien di situs web.

### Tajuk WOFF2
Header WOFF terdiri dari tanda pengenal yang menunjukkan jenis data yang disertakan dalam file. Header WOFF beserta field-nya adalah sebagai berikut.

|Jenis|Nama Bidang|Deskripsi|
---|---|---|
|UInt32|tanda tangan |0x774F4632 'wOF2' |
|UInt32| rasa |Versi sfnt dari font masukan.|
|UInt32| panjang |Ukuran total file WOFF.|
|UInt16| numTables |Jumlah entri dalam direktori tabel font.|
|UInt16| dilindungi undang-undang | Dicadangkan; disetel ke nol.|
|UInt32| totalSfntSize |Ukuran total yang diperlukan untuk data font yang tidak terkompresi, termasuk header sfnt, direktori, dan tabel font (termasuk padding).|
|UInt32| totalCompressedSize Total panjang blok data terkompresi.|
|UInt16| mayorVersion |Versi utama dari file WOFF.|
|UInt16| minorVersion |Versi kecil dari file WOFF.|
|UInt32| metaOffset |Offset ke blok metadata, dari awal file WOFF.|
|UInt32| metaLength |Panjang blok metadata terkompresi.|
|UInt32| metaOrigLength |Ukuran blok metadata yang tidak terkompresi.|
|UInt32| privOffset |Offset ke blok data pribadi, dari awal file WOFF.|
|UInt32| privLength |Panjang blok data pribadi.|


## Referensi
 * [Format Berkas w3 WOFF2](https://www.w3.org/TR/WOFF2/)

