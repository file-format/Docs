{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "ekstensi", "file cdb", "format file cdb", "Jenis File Basis Data", "Format File Basis Data", "apa itu file cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file CDB dan API yang dapat membuat dan membuka file CDB.",
  "title" :"CDB - File Basis Data Konstan",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Apa itu file CDB?
File CDB digunakan dalam aplikasi penting seperti email. CDB adalah singkatan dari "constant database", paket yang cepat, andal, dan sederhana untuk membuat atau membaca database konstan. Penggantian basis data aman terhadap kerusakan sistem. Pengguna tidak perlu menjeda selama penulisan ulang. CDB berfungsi sebagai array asosiatif (on-disk), memetakan kunci ke nilai, dan memungkinkan beberapa nilai disimpan dalam satu kunci.

## Format File CDB
Format file CDB menyimpan angka, offset, panjang, dan nilai hash dalam format little endian sebagai bilangan bulat 32-bit yang tidak ditandatangani. Kunci dan data dianggap sebagai string byte buram tanpa perlakuan khusus. Di awal database, header ukuran tetap mewakili 256 tabel hash dengan mencantumkan posisinya di dalam file dan panjangnya di slot. Biasanya data disimpan sebagai urutan record, setiap record menyimpan panjang kunci, panjang data, kunci, dan data. Tidak ada aturan pengurutan atau perataan. Catatan diikuti oleh satu set 256 tabel hash dengan panjang yang bervariasi. Karena nol adalah panjang yang valid, mungkin ada kurang dari 256 tabel hash yang disimpan secara fisik dalam database, tetapi tidak ada yang dianggap 256 tabel. Tabel hash terdiri dari serangkaian slot, yang masing-masing berisi nilai hash dan catatan offset. "Slot kosong" memiliki offset nol.

### Struktur
Database CDB terdiri dari seluruh dataset dalam satu file komputer. Ini berisi tiga bagian:
- Header berukuran tetap
- Data
- Satu set tabel hash.

Pencarian hanya tersedia untuk kunci yang tepat. Pencarian bertindak menggunakan algoritme berikut:

- Hash kuncinya.
- Tentukan di mana tabel hash dan slot catatan ini harus ditempatkan.
- Uji slot yang ditunjukkan di tabel hash.

Untuk pencarian kunci dengan lebih dari satu nilai, nilai tambahan dapat ditemukan hanya dengan melanjutkan pencarian di slot berikutnya.

#### Fitur

Struktur database CDB menyediakan beberapa fitur:

##### Pencarian cepat
Pencarian yang berhasil dalam database besar biasanya hanya membutuhkan dua akses disk dan pencarian yang gagal hanya membutuhkan satu akses.
##### Overhead rendah
Database menggunakan 2048 byte, 24 byte per record dan ruang untuk kunci dan data.
##### Tidak ada batasan acak
CDB dapat mengelola database apa pun hingga 4 gigabyte. Karena tidak ada batasan lain, catatan bahkan tidak harus masuk ke dalam memori. Database disimpan dalam format independen mesin.
##### Penggantian basis data atom cepat
Perintah **cdbmake** dapat menulis ulang seluruh database menjadi dua kali lipat, lebih cepat daripada paket hashing lainnya.
##### Pembuangan database cepat
**cdbdump** dapat mencetak konten database dalam format yang kompatibel dengan cdbmake.


## Referensi ##

* [cdb (perangkat lunak) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [spesifikasi CDB](http://cr.yp.to/cdb.html)

