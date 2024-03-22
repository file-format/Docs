{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Format File", "Buka", "Baca", "Buat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DWF dan API yang dapat membuat dan membuka file DWF.",
  "title" :"Format File DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DWF?

Design Web Format (DWF) mewakili gambar 2D/3D dalam format terkompresi untuk melihat, meninjau, atau mencetak file desain. Ini berisi grafik dan teks sebagai bagian dari data desain dan mengurangi ukuran file karena formatnya yang terkompresi. Ukuran file yang dikurangi membuat distribusi dan komunikasi data desain yang kaya menjadi efisien. DWF tidak mengharuskan penerima untuk mengetahui tentang penggunaan perangkat lunak CAD yang membuat gambar aslinya. Konten format file DWF bisa sederhana dan hanya menyertakan satu lembar atau cukup rumit untuk memiliki font, warna, dan gambar.

## Sejarah Singkat ##

Autodesk memperkenalkan format file DWF pada tahun 1995 sebagai bagian dari Netscape Navigation plug-in, WHIP. Formatnya berevolusi dari format 2D saja untuk memasukkan konten 3D seiring berjalannya waktu. Banyak aplikasi pihak ketiga juga menggunakan format ini.

## Format File DWF ##

DWF adalah format terbuka dan aman yang dirancang khusus untuk berbagi data desain teknik yang kaya. Itu tidak tergantung pada perangkat lunak aplikasi asli, perangkat keras, dan sistem operasi yang digunakan untuk membuat data desain tersebut. Ini memungkinkan anggota tim yang tidak menggunakan aplikasi CAD untuk berpartisipasi dalam proses digital dengan melihat desain bangunan, GIS, atau produk. Arsip file DWF terdiri dari beberapa file XML dan biner yang dikemas bersama dalam arsip terkompresi yang dibuat dengan kompresi [ZIP](/id/compression/zip/). Anda dapat mengganti nama ekstensi file DWF menjadi ZIP dan melihat konten file. Paket DWF dapat berisi banyak jenis data desain seperti grafik 2D, grafik 3D, metadata paket dan bagian, dan file sumber daya lainnya.

**File metadata DWF** – File XML yang berisi informasi terkait metadata dan struktur (penulis, judul, waktu pembuatan, dependensi bagian, pengurutan bagian, deskripsi file sumber daya, peran, tipe mime, dll.) dan berkaitan dengan bagian (halaman informasi, metadata desain, dll.). Metadata struktural digunakan untuk membuat objek logis (koleksi file untuk mewakili bagian atau halaman, dll.).

**File sumber daya** – file media atau konten lain yang direferensikan dari metadata paket/bagian dan biasanya berupa presentasi data desain dalam berbagai format (ZGL, W2D, [JPG](/id/image/jpeg/), [PNG](/id/image/png/), AVI, XML, [TXT](/id/word-processing/txt/), [DOC](/id/word-processing/doc/), dll.)

### Detail Format File ###

File DWF disusun menjadi tiga bagian utama seperti yang ditunjukkan di bawah ini.

* Tajuk identifikasi file
* File blok data
* Trailer terminasi file

#### Header Pengidentifikasi Berkas ####

Header pengidentifikasi file memungkinkan identifikasi file DWF oleh aplikasi. Itu juga mengidentifikasi versi spesifikasi DWF mana yang digunakan untuk menyandikan file. Ini adalah header 12 byte yang disusun sebagai berikut:


|Bita|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Karakter|(|D|W|F|(spasi)|V|0|0|.|3|0|)

Berikut adalah ringkasan dari tabel ini:

* Enam byte pertama dari header selalu mewakili karakter ASCII "(DWF V"
* 5 byte berikut berisi informasi tentang nomor versi misal "00.30" dengan format nilai versi mayor dan minor

Aplikasi yang membuat file DWF harus menentukan nomor versi serendah mungkin yang perlu didukung oleh aplikasi pembaca agar dapat menggunakan data dengan benar.

#### Blok Data File ####

Blok data file dimulai pada byte ke-13 dari file DWF, dan merupakan serangkaian pasangan opcode dan operan, seperti pada tabel berikut.

|Bidang 1|Bidang 2|Bidang 3|Bidang 4|Bidang 5|Bidang 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operan

File DWF dapat berisi pasangan opcode-operan sebagai ASCII yang dapat dibaca serta kode biner atau campuran keduanya. Semua operasi DWF memiliki bentuk opcode/operan ASCII yang dapat dibaca, dan sebagian besar operasi juga memiliki bentuk opcode/operan biner yang dikodekan. Opcode dalam satu byte memungkinkan lebih dari 200 operasi. ASCII yang diperluas dan biner yang diperluas adalah kasus luar biasa. Nilai Opcode dapat berkisar dari 0-255 dengan beberapa pengecualian. Kecuali untuk dua jenis opcode khusus yang diperluas ASCII dan biner yang diperluas, pembaca file harus tahu cara menghitung panjang operan.

##### Opcode Terlarang #####

Representasi ASCII untuk yang berikut ini tidak dapat digunakan sebagai opcode:

Representasi ASCII berikut tidak dapat digunakan sebagai opcode:

* Ruang (0x20)
* Tab (0x09)
* Tanda hubung (0x2D)
* Angka ASCII 0-9 (0x30 - 0x39)
* Kereta kembali (0x0D)
* Umpan baris (0x0A)
* Tanda Petik Tunggal (0x27)
* Tanda kutip ganda (0x22)
* Periode (0x2E)
* Kurung (0x28 dan 0x29)
* Kurung keriting (0x7B dan 0x7D)
* Kurung persegi (0x5B dan 0x5D)
* Garis miring ke belakang (0x5C)

#### Trailer Pengakhiran File ####

Trailer penghentian file untuk DWF hanyalah sebuah opcode khusus yang menunjukkan akhir file. Beberapa aplikasi dapat menyimpan data non-DWF mengikuti opcode penghentian. Cuplikannya seperti yang ditunjukkan di bawah ini:


|Bita|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Karakter|(|E|n|d|0|f|D|W|F|)

## Referensi ##

* [DWF - Oleh Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Format Data WHIP](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

