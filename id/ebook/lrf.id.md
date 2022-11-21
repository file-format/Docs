{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "file", "ekstensi", "format", "eBuku", "Buku digital" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file LRF dan API yang dapat membuat dan membuka file LRF.",
  "title" :"Format File LRF - File Pembaca Portabel Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Apa itu file LRF?

File dengan ekstensi .lrf adalah file Broad Band eBook (BBeB) yang berisi data untuk Sony BBeB, termasuk data teks, gambar, dan paginasi. File disimpan dalam format biner terkompresi yang berisi header, sejumlah objek tertentu, dan indeks objek. File LRF dan LRX menyertakan dua format buku BBeB yang tersedia. File LRF tidak dienkripsi dan dapat dikompilasi dari file [LRX](/id/ebook/lrf/). File LRF dapat dikonversi dari beberapa jenis file lain termasuk PDF dan HTML. Jika komputer Anda tidak dapat membuka file LRF, Anda mungkin tidak menginstal perangkat lunak untuk membuka atau mengedit file LRF. Program yang dapat membuka file LRF adalah Calibre, BookDesigner, Makelrf dan Canon Book Creator untuk Windows, Calibre untuk Linux, Calibre, dan Sony Reader untuk Macintosh.

## Sejarah Singkat

Jenis file LRF pertama-tama dikaitkan dengan Line Rider oleh [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). The Line Rider adalah mainan fisika internet dan ditemukan pada bulan September 2006 oleh seorang mahasiswa Slovenia, Boštjan Čadež. eReader eBook merek Sony (seperti pembaca Sony PRS-500 dan Sony Librie) menggunakan ekstensi file LRF untuk dokumen dan teks mereka. Jenis file berpemilik ini sekarang sudah usang, serta file LRS dan LRX terkait. Ketiga jenis file tersebut merupakan BroadBand eBook (BBeB) yang dihentikan pada tahun 2010 ketika Sony mulai menjual ebook mereka dalam format EPUB.

## Format File LRF

Spesifikasi detail format file LRF tersedia di [arsip web](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). File LRF terdiri dari:
* sebuah tajuk
* sejumlah objek
* indeks objek.

Semua nilai ini dalam urutan Intel (LSB pertama).

### Tajuk LRF

|Offset (hex) |Ukuran(byte) |Nama/makna| Contoh nilai|
---|---|---|---|
|0 |8| Tanda Tangan LRF| 4C 00 52 00 46 00 00 00 = "LRF" di Unicode|
|8 |2| versi?| 999 di sebagian besar file|
|A |2| "Enkripsi-Psuedo" |byte kunci 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| BilanganObjek |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| tidak diketahui| 0|
|24 |1| Bendera| (16 - belakang ke depan, 1 = depan ke belakang) 16|
|25 |1| tidak diketahui |(padding?) 0|
|26 |2| tidak diketahui| 1600|
|28 |2| tidak diketahui| (pengisian?) 0|
|2A |2| Tinggi?| 600|
|2C |2| Lebar?| 800|
|2E |1| tidak diketahui| 24|
|2F |1| tidak diketahui |(padding?) 0|
|30 |0x14| tidak diketahui| nol|
|44 |4| ID objek hanya dari objek PlaneStream (0x1E)| 0x0042|
|48 |4| tidak diketahui |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referensi

* [Format File LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Oleh Wikipedia](https://en.wikipedia.org/wiki/BBeB)

