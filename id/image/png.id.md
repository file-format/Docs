{
  "date" : "2019-10-11",
  "keywords" :[ "file png", "format file png", "apa itu file png", "file", "contoh png", "ekstensi file png", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File PNG - File Gambar Raster",
  "description":"Pelajari tentang format file PNG dan API yang dapat membuat dan membuka file PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PNG?

File **PNG** (Portable Network Graphics) adalah format file gambar raster yang menggunakan kompresi lossless. Format file ini dibuat sebagai pengganti Graphics Interchange Format ([GIF](/id/image/gif/)) dan tidak memiliki batasan hak cipta. Namun, format file PNG tidak mendukung animasi. Format file PNG mendukung kompresi gambar lossless yang membuatnya populer di kalangan penggunanya. Seiring berjalannya waktu, PNG telah berkembang sebagai salah satu format file gambar yang banyak digunakan.

## Sejarah Singkat Format File PNG

Alasan utama di balik pembuatan format file PNG adalah algoritma kompresi yang dipatenkan, Lempel-Ziv-Welch, yang digunakan dalam format file GIF. Ini bersama dengan batasan GIF lainnya menciptakan kebutuhan untuk mengganti format file [**GIF**](/id/image/gif/). Proposal dan nama pertama untuk format file PNG datang pada Januari 1995. Peristiwa penting sehubungan dengan format file PNG tercantum di bawah ini:

* Oktober 1996: Spesifikasi PNG Versi 1.0 dirilis dan kemudian muncul sebagai [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Hal yang sama menjadi Rekomendasi W3C pada Oktober 1996.
* Desember 1998: Versi 1.1, dengan beberapa perubahan kecil dan penambahan tiga bagian baru, dirilis.
* Agustus 1999: Versi 1.2, menambahkan satu potongan ekstra, dirilis.
* November 2003: PNG menjadi Standar Internasional (ISO/IEC 15948:2003). Versi PNG ini hanya sedikit berbeda dari versi 1.2 dan tidak menambahkan potongan baru.
* Maret 2004: ISO/IEC 15948:2004

## Perbandingan Fungsional GIF dan PNG

Format file PNG dirancang agar sederhana dan portabel, tidak terbebani secara hukum, dapat dipertukarkan, fleksibel, dan kuat. Tabel berikut mencantumkan fitur GIF yang diwariskan oleh format file PNG selain fitur baru.

|Fitur|GIF|PNG|
---|---|---|
|Gambar warna indeks hingga 256 warna|Ya|Ya|
|Dukungan untuk streaming|Ya|Ya|
|Transparansi|Ya|Ya|
|Informasi tambahan|Ya|Ya|
|Kemandirian Perangkat Keras dan Platform|Ya|Ya|
|Efektif|Ya|Ya|
|Gambar truecolor hingga 48 bit per piksel|Tidak|Ya|
|Gambar skala abu-abu hingga 16 bit per piksel|Tidak|Ya|
|Saluran alfa penuh (topeng transparansi umum)|Tidak|Ya|
|Informasi gamma gambar|Tidak|Ya|
|Keandalan|Tidak|Ya|
|Presentasi awal lebih cepat|Tidak|Ya|

## Struktur Berkas PNG

Hampir semua Sistem Operasi memiliki dukungan untuk membuka file PNG. Misalnya, penampil Microsoft Windows memiliki kemampuan untuk membuka file PNG karena OS secara default memiliki dukungan yang tersedia sebagai bagian dari instalasi. File PNG terdiri dari `tanda tangan` PNG diikuti oleh serangkaian //potongan//.

### Tajuk Berkas PNG

Delapan byte pertama file PNG selalu berisi nilai (desimal) berikut:

{{{137 80 78 71 13 10 26 10 }}}

Tanda tangan ini menunjukkan bahwa sisa file berisi satu gambar PNG, yang terdiri dari serangkaian potongan yang dimulai dengan potongan IHDR dan diakhiri dengan potongan IEND.

### Potongan ###

Setiap potongan terdiri dari empat bagian:

**Panjang:** Bilangan bulat tak bertanda 4 byte yang memberikan jumlah byte dalam bidang data potongan. Panjangnya hanya menghitung bidang data, bukan itu sendiri, kode tipe potongan, atau CRC. Nol adalah panjang yang valid. Meskipun encoder dan decoder harus memperlakukan panjang sebagai unsigned, nilainya tidak boleh melebihi 231 byte.

**Chunk Type:** Kode tipe chunk 4-byte. Untuk kenyamanan dalam mendeskripsikan dan memeriksa file PNG, kode jenis dibatasi untuk terdiri dari huruf ASCII huruf besar dan kecil (AZ dan az, atau desimal 65-90 dan 97-122). Namun, pembuat enkode dan dekoder harus memperlakukan kode sebagai nilai biner tetap, bukan string karakter. Misalnya, tidak tepat untuk menyatakan kode jenis IDAT dengan ekuivalen EBCDIC dari huruf tersebut. Konvensi penamaan tambahan untuk tipe chunk dibahas di bagian berikutnya.

**Data Potongan:** Byte data yang sesuai dengan jenis potongan, jika ada. Panjang kolom ini bisa nol.

**CRC:** CRC (Cyclic Redundancy Check) 4-byte dihitung pada byte sebelumnya dalam potongan, termasuk kode jenis potongan dan bidang data potongan, tetapi tidak termasuk bidang panjang. CRC selalu ada, bahkan untuk potongan yang tidak berisi data.

Panjang data potongan dapat berupa sejumlah byte hingga maksimum; oleh karena itu, pelaksana tidak dapat berasumsi bahwa potongan disejajarkan pada batas yang lebih besar dari byte.

Potongan dapat muncul dalam urutan apa pun, tunduk pada batasan yang ditempatkan pada setiap jenis potongan. (Salah satu batasan penting adalah bahwa IHDR harus muncul terlebih dahulu dan IEND harus muncul terakhir; sehingga potongan IEND berfungsi sebagai penanda akhir file.) Beberapa potongan dari jenis yang sama dapat muncul, tetapi hanya jika diizinkan secara khusus untuk jenis tersebut.

#### Jenis Potongan

Tipe Chunk dikategorikan ke dalam chunk **Kritis** dan **Pendukung** berdasarkan nilai ASCII peka huruf besar-kecil 4-byte yang ditetapkan ke Tipe Chunk. Semua implementasi harus memahami dan berhasil membuat potongan kritis standar. Gambar PNG yang valid harus berisi potongan IHDR, satu atau beberapa potongan IDAT, dan potongan IEND.

### Kompresi

Metode kompresi PNG 0 (satu-satunya metode kompresi yang saat ini ditentukan untuk PNG) menentukan kompresi deflate/inflate dengan jendela geser paling banyak 32768 byte. Kompresi mengempis adalah turunan LZ77 yang digunakan dalam zip, gzip, pkzip, dan program terkait. Penelitian ekstensif telah dilakukan untuk mendukung status bebas patennya. Data terkompresi dalam aliran data zlib disimpan sebagai serangkaian blok, yang masing-masing dapat mewakili data mentah (tidak terkompresi), data terkompresi LZ77 yang dikodekan dengan kode Huffman tetap, atau data terkompresi LZ77 yang dikodekan dengan kode Huffman kustom. Bit penanda di blok terakhir mengidentifikasinya sebagai blok terakhir, memungkinkan dekoder mengenali akhir aliran data terkompresi.

#### Penyaringan Pra-Kompresi

Filter pra-kompresi diterapkan untuk menyiapkan data gambar untuk kompresi optimal. Metode filter PNG mendefinisikan lima jenis filter dasar sebagai berikut:

|Jenis Filter|Nama|Nilai Prediksi|
---|---|---|
|0|Tidak ada|Scanline ditransmisikan tanpa modifikasi|
|1|Sub|Mentransmisikan perbedaan antara setiap byte dan nilai byte yang sesuai dari piksel sebelumnya.|
|2|Up|Filter Up() sama seperti filter Sub() kecuali bahwa piksel tepat di atas piksel saat ini, bukan hanya di sebelah kirinya, digunakan sebagai prediktor.|
|3|Rata-Rata|Filter Rata-Rata() menggunakan rata-rata dari dua piksel tetangga (kiri dan atas) untuk memprediksi nilai piksel.|
|4|Paeth|Filter Paeth() menghitung fungsi linier sederhana dari tiga piksel tetangga (kiri, atas, kiri atas), lalu memilih sebagai prediktor piksel tetangga yang paling dekat dengan nilai yang dihitung.|

Algoritme pemfilteran diterapkan ke `byte`, bukan ke piksel, terlepas dari kedalaman bit atau jenis warna gambar. Algoritma penyaringan bekerja pada urutan byte yang dibentuk oleh scanline. Jika gambar menyertakan saluran alfa, data alfa difilter dengan cara yang sama seperti data gambar.

Saat gambar diinterlac, setiap lintasan pola interlace diperlakukan sebagai gambar independen untuk keperluan pemfilteran. Filter bekerja pada urutan byte yang dibentuk oleh piksel yang benar-benar ditransmisikan selama lintasan, dan "garis pindaian sebelumnya" adalah yang sebelumnya ditransmisikan dalam lintasan yang sama, bukan yang berdekatan dalam gambar lengkap. Perhatikan bahwa subgambar yang ditransmisikan dalam satu lintasan selalu berbentuk persegi panjang, tetapi lebar dan/atau tingginya lebih kecil daripada gambar lengkap. Pemfilteran tidak diterapkan saat subgambar ini kosong.

## Referensi ##

* [PNG - Beranda](http://www.libpng.org/pub/png/)

