{
  "date" : "2021-08-09",
  "keywords" :[ "file cso", "format file cso", "apa itu file cso", "file", "contoh cso", "ekstensi file cso", "ekstensi", "format", "iso", "kompresi DAX " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file CSO dan API yang dapat membuat dan membuka file CSO.",
  "title" :"CSO - Gambar Disk ISO Terkompresi",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Apa itu file CSO?

File dengan ekstensi .cso adalah file gambar ISO terkompresi. CSO adalah alternatif dari metode kompresi DAX; juga dikenal sebagai CISO; adalah metode pertama untuk mengompres file [ISO](/id/compression/iso/) dan biasanya merupakan metode yang disukai untuk mengarsipkan barang-barang PlayStation Portable. Format ini menggunakan kompresi Deflate, yang dapat mencakup hingga sembilan lapisan kompresi. Perangkat lunak seperti Prometheus dan YACC digunakan untuk membuat gambar.

## format file CSO

Format file CSO adalah metode kompresi pertama untuk ISO untuk menghemat lebih banyak ruang memori. Peningkatan dilakukan dari waktu ke waktu untuk kompresi yang lebih baik. CSO menggunakan kompresi Deflate yang memiliki sembilan level preset, biasanya setiap level dapat menangani 2 blok KiB secara individual. Sementara tingkat kompresi tertinggi dapat memperlambat dan waktu muat yang lama dalam perangkat lunak yang sangat bergantung pada streaming disk, tingkat yang lebih rendah juga dapat melakukan kompresi yang substansial.

### struktur file CSO

Format file CSO berisi header 24-byte, blok data, dan tabel indeks. Little-endian diasumsikan untuk bidang yang lebih besar dari satu byte. Endianness arsitektur PlayStation Portable diberikan di bawah ini.

#### Judul

| Offset (byte) | Nama | Ukuran (byte) | Tujuan |
----------|----------|--------------|---------|
| 0x0 | Sihir | 4 | Selalu CISO, atau 0x4F534943 saat dibaca sebagai integer 32-bit. Bidang ini digunakan untuk mengidentifikasi file CSO. Perhatikan bahwa bidang ini dapat berbeda untuk turunan CSO lainnya, misalnya ZSO menggunakan kode ajaib ZISO. |
| 0x4 | Ukuran tajuk | 4 | Untuk format file "v1" CSO asli, bidang ini diabaikan dan karenanya tidak harus akurat. Namun, format "v2" dan ZSO mengharuskan kolom ini selalu berukuran 0x18 (24 byte). |
| 0x8 | Ukuran tidak terkompresi | 8 | Ukuran ISO asli yang tidak dikompresi dalam byte. |
| 0x10 | Ukuran blok | 4 | Ukuran setiap blok data dalam byte sebelum kompresi. Biasanya 2048 byte, sama dengan ukuran setiap sektor ISO 9660. |
| 0x14 | Versi | 1 | Versi format file yang digunakan. Untuk format "v1", nilainya bisa 0 atau 1. Untuk format "v2", ini harus 2. Selain itu, format ZSO mengharuskan ini menjadi 1. |
| 0x15 | Perataan indeks | 1 | Penyelarasan setiap entri indeks, ditentukan dalam bit. |
| 0x16 | Dicadangkan | 2 | Kolom ini tidak digunakan. Dalam format "v1", kolom ini diabaikan dan mungkin berisi nilai arbitrer. Dalam format "v2", kolom ini harus nol. |

#### Tabel indeks

Tabel indeks berisi beberapa entri 4-byte, yang menunjukkan posisi setiap blok data, dan tambahan, entri terakhir yang menunjuk ke akhir file.
Isi setiap entri adalah sebagai berikut:
| Sedikit | Panjang | Topeng | Nama | Tujuan |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFF | Posisi | Bidang ini, saat digeser ke kiri oleh perataan indeks yang diberikan di header, memberikan posisi di mana blok data dimulai. |
| 31 | 1 | 0x80000000 | Jenis kompresi | Format ZSO memiliki semantik yang serupa, hanya saja 0 mewakili LZ4, bukan Deflate. Dalam format "v2". Blok secara implisit dianggap tidak terkompresi jika ukuran blok sama dengan atau lebih besar dari ukuran blok yang ditentukan di header file. |

#### Blok data

Blok data terdiri dari data yang tidak terkompresi atau terkompresi. Ukuran sebuah balok dihitung dengan mendapatkan posisinya, lalu mengurangkannya dari posisi balok berikutnya. Jika penyelarasan indeks lebih besar dari nol, kemungkinan besar ukuran blok lebih besar dari data yang dimilikinya.


## Referensi

* [CSO - oleh Wikipedia](https://en.wikipedia.org/wiki/.CSO)


